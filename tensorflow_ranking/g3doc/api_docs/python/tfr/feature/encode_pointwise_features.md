<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tfr.feature.encode_pointwise_features" />
<meta itemprop="path" content="Stable" />
</div>

# tfr.feature.encode_pointwise_features

<!-- Insert buttons and diff -->

<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/ranking/tree/master/tensorflow_ranking/python/feature.py">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>

Returns dense tensors from pointwise features using feature columns.

```python
tfr.feature.encode_pointwise_features(
    features, context_feature_columns, example_feature_columns,
    mode=tf.estimator.ModeKeys.PREDICT, scope=None
)
```

<!-- Placeholder for "Used in" -->

#### Args:

*   <b>`features`</b>: (dict) mapping feature names to 2-D tensors, possibly
    obtained from input_fn.
*   <b>`context_feature_columns`</b>: (dict) context feature names to columns.
*   <b>`example_feature_columns`</b>: (dict) example feature names to columns.
*   <b>`mode`</b>: (`estimator.ModeKeys`) Specifies if this is training,
    evaluation or inference. See `ModeKeys`.
*   <b>`scope`</b>: (str) variable scope for the per column input layers.

#### Returns:

*   <b>`context_features`</b>: (dict) A mapping from context feature names to
    dense 2-D tensors of shape [batch_size, ...].
*   <b>`example_features`</b>: (dict) A mapping from example feature names to
    dense 3-D tensors of shape [batch_size, 1, ...].
