---
title: glIsEnabled-Funktion (Gl.h)
description: Die gllsEnabled-Funktion testet, ob eine Funktion aktiviert ist.
ms.assetid: 18df5a6f-dc21-434d-a2e8-2c58597df037
keywords:
- glIsEnabled-Funktion OpenGL
topic_type:
- apiref
api_name:
- glIsEnabled
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3237cedc1daeffa3fd47fd50b9b19d79ebad3acbf53bdd7929b70dad4093a7a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493400"
---
# <a name="glisenabled-function"></a>glIsEnabled-Funktion

Die **gllsEnabled-Funktion testet,** ob eine Funktion aktiviert ist.

## <a name="syntax"></a>Syntax


```C++
GLboolean WINAPI glIsEnabled(
   GLenum cap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cap* 
</dt> <dd>

Eine symbolische Konstante, die eine OpenGL-Funktion angibt. Die folgenden Funktionen werden akzeptiert.



| Wert                                                                                                                                                                                                    | Bedeutung                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span><dl> <dt>**GL \_ ALPHA \_ TEST**</dt> </dl>                                           | Siehe [ **glAlphaFunc**](glalphafunc.md)<br/>                                                                                                   |
| <span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span><dl> <dt>**GL \_ AUTO \_ NORMAL**</dt> </dl>                                        | Siehe [ **glEvalCoord**](glevalcoord-functions.md)<br/>                                                                                         |
| <span id="GL_BLEND"></span><span id="gl_blend"></span><dl> <dt>**GL \_ BLEND**</dt> </dl>                                                           | Siehe [ **glBlendFunc**](glblendfunc.md)<br/>                                                                                                   |
| <span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span><dl> <dt>**GL \_ CLIP \_ PLANE *i**</dt> </dl> | Siehe [ **glClipPlane**](glclipplane.md)<br/>                                                                                                   |
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**GL \_ COLOR \_ ARRAY**</dt> </dl>                                        | Siehe [ **glColorPointer.**](glcolorpointer.md)<br/>                                                                                             |
| <span id="GL_COLOR_LOGIC_OP"></span><span id="gl_color_logic_op"></span><dl> <dt>**GL \_ COLOR \_ LOGIC \_ OP**</dt> </dl>                              | Weitere Informationen finden Sie [ **unter glLogicOp.**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span><dl> <dt>**GL \_ COLOR \_ MATERIAL**</dt> </dl>                               | Siehe [ **glColorMaterial.**](glcolormaterial.md)<br/>                                                                                           |
| <span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span><dl> <dt>**GL \_ CULL \_ FACE**</dt> </dl>                                              | Siehe [ **glCullFace.**](glcullface.md)<br/>                                                                                                     |
| <span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span><dl> <dt>**\_ \_ GL-TIEFENTEST**</dt> </dl>                                           | Siehe [**glDepthFunc**](gldepthfunc.md) und [**glDepthRange.**](gldepthrange.md)<br/>                                                          |
| <span id="GL_DITHER"></span><span id="gl_dither"></span><dl> <dt>**GL \_ DITHER**</dt> </dl>                                                        | Siehe [ **glEnable**](glenable.md)<br/>                                                                                                         |
| <span id="GL_FOG"></span><span id="gl_fog"></span><dl> <dt>**GL \_ VERSCHENKTE**</dt> </dl>                                                                 | Siehe [ **glFog**](glfog.md)<br/>                                                                                                               |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**GL \_ INDEX \_ ARRAY**</dt> </dl>                                        | Siehe [ **glIndexPointer**](glindexpointer.md)<br/>                                                                                             |
| <span id="GL_INDEX_LOGIC_OP"></span><span id="gl_index_logic_op"></span><dl> <dt>**GL \_ INDEX \_ LOGIC \_ OP**</dt> </dl>                              | Weitere Informationen finden Sie [ **unter glLogicOp.**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span><dl> <dt>**GL \_ LIGHT *i**</dt> </dl>                      | Siehe [**glLightModel**](gllightmodel-functions.md) und [**glLight.**](gllight-functions.md)<br/>                                              |
| <span id="GL_LIGHTING"></span><span id="gl_lighting"></span><dl> <dt>**GL \_ LIGHTING**</dt> </dl>                                                  | Siehe [**glMaterial,**](glmaterial-functions.md) [**glLightModel**](gllightmodel-functions.md)und [**glLight.**](gllight-functions.md)<br/> |
| <span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span><dl> <dt>**GL \_ LINE \_ SMOOTH**</dt> </dl>                                        | Siehe [ **glLineWidth**](gllinewidth.md)<br/>                                                                                                   |
| <span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span><dl> <dt>**GL \_ LINE \_ STIPPLE**</dt> </dl>                                     | Siehe [ **glLineStipple**](gllinestipple.md)<br/>                                                                                               |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**GL \_ MAP1 \_ COLOR \_ 4**</dt> </dl>                                    | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**GL \_ MAP1 \_ INDEX**</dt> </dl>                                           | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**GL \_ MAP1 \_ NORMAL**</dt> </dl>                                        | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1**</dt> </dl>           | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2**</dt> </dl>           | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3**</dt> </dl>           | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4**</dt> </dl>           | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**GL \_ MAP1 \_ VERTEX \_ 3**</dt> </dl>                                 | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**GL \_ MAP1 \_ VERTEX \_ 4**</dt> </dl>                                 | Siehe [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**GL \_ MAP2 \_ COLOR \_ 4**</dt> </dl>                                    | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**GL \_ MAP2 \_ INDEX**</dt> </dl>                                           | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**GL \_ MAP2 \_ NORMAL**</dt> </dl>                                        | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1**</dt> </dl>           | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2**</dt> </dl>           | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3**</dt> </dl>           | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4**</dt> </dl>           | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**GL \_ MAP2 \_ VERTEX \_ 3**</dt> </dl>                                 | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**GL \_ MAP2 \_ VERTEX \_ 4**</dt> </dl>                                 | Siehe [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**GL \_ NORMAL \_ ARRAY**</dt> </dl>                                     | Siehe [ **glNormalPointer.**](glnormalpointer.md)<br/>                                                                                           |
| <span id="GL_NORMALIZE"></span><span id="gl_normalize"></span><dl> <dt>**GL \_ NORMALIZE**</dt> </dl>                                               | Siehe [ **glNormal.**](glnormal-functions.md)<br/>                                                                                               |
| <span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span><dl> <dt>**GL \_ POINT \_ SMOOTH**</dt> </dl>                                     | Siehe [ **glPointSize**](glpointsize.md)<br/>                                                                                                   |
| <span id="GL_POLYGON_OFFSET_FILL"></span><span id="gl_polygon_offset_fill"></span><dl> <dt>**GL \_ POLYGON \_ OFFSET \_ FILL**</dt> </dl>               | Siehe [ **glPolygonOffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_LINE"></span><span id="gl_polygon_offset_line"></span><dl> <dt>**GL \_ POLYGON \_ OFFSET \_ LINE**</dt> </dl>               | Siehe [ **glPolygonOffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_POINT"></span><span id="gl_polygon_offset_point"></span><dl> <dt>**GL \_ POLYGON \_ OFFSET \_ POINT**</dt> </dl>            | Siehe [ **glPolygonOffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span><dl> <dt>**GL \_ POLYGON \_ SMOOTH**</dt> </dl>                               | Siehe [ **glPolygonMode.**](glpolygonmode.md)<br/>                                                                                               |
| <span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span><dl> <dt>**GL \_ POLYGON \_ STIPPLE**</dt> </dl>                            | Siehe [ **glPolygonStipple**](glpolygonstipple.md)<br/>                                                                                         |
| <span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span><dl> <dt>**GL \_ \_ SCISSOR-TEST**</dt> </dl>                                     | Siehe [ **glScissor**](glscissor.md)<br/>                                                                                                       |
| <span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span><dl> <dt>**GL \_ \_ STENCIL-TEST**</dt> </dl>                                     | Siehe [**glStencilFunc**](glstencilfunc.md) und [**glStencilOp.**](glstencilop.md)<br/>                                                        |
| <span id="GL_TEXTURE_1D"></span><span id="gl_texture_1d"></span><dl> <dt>**GL \_ TEXTURE \_ 1D**</dt> </dl>                                           | Siehe [ **glTexImage1D**](glteximage1d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_2D"></span><span id="gl_texture_2d"></span><dl> <dt>**GL \_ TEXTURE \_ 2D**</dt> </dl>                                           | Siehe [ **glTexImage2D**](glteximage2d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**GL \_ TEXTURE \_ COORD \_ ARRAY**</dt> </dl>               | Siehe [ **glTexCoordPointer**](gltexcoordpointer.md)<br/>                                                                                       |
| <span id="GL_TEXTURE_GEN_Q"></span><span id="gl_texture_gen_q"></span><dl> <dt>**GL \_ TEXTURE \_ GEN \_ Q**</dt> </dl>                                 | Siehe [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_R"></span><span id="gl_texture_gen_r"></span><dl> <dt>**GL \_ TEXTURE \_ GEN \_ R**</dt> </dl>                                 | Siehe [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_S"></span><span id="gl_texture_gen_s"></span><dl> <dt>**GL \_ TEXTURE \_ GEN \_ S**</dt> </dl>                                 | Siehe [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_T"></span><span id="gl_texture_gen_t"></span><dl> <dt>**GL \_ TEXTURE \_ GEN \_ T**</dt> </dl>                                 | Siehe [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**GL \_ VERTEX \_ ARRAY**</dt> </dl>                                     | Siehe [ **glVertexPointer**](glvertexpointer.md)<br/>                                                                                           |



 

</dd> </dl>

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *cap* war kein akzeptierter Wert.<br/>                                                                                           |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **gllsEnabled-Funktion** gibt GL \_ TRUE zurück, wenn *cap* eine aktivierte Funktion ist, und \_ gibt andernfalls GL FALSE zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





