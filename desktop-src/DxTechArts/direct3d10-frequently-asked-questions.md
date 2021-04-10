---
title: Häufig gestellte Fragen zu Direct3D 10
description: Dieser Artikel enthält einige häufig gestellte Fragen im Zusammenhang mit Direct3D 10 aus der Sicht eines Entwicklers, der eine vorhandene Anwendung von Direct3D 9 (d3d9) auf Direct3D 10 (d3d10) portieren soll.
ms.assetid: da3022ca-b120-d0d7-6747-65b946dbc73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae228923715400e5ba7e4f795e3ea6bfacfd98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101898"
---
# <a name="direct3d-10-frequently-asked-questions"></a>Häufig gestellte Fragen zu Direct3D 10

Dieser Artikel enthält einige häufig gestellte Fragen im Zusammenhang mit Direct3D 10 aus der Sicht eines Entwicklers, der eine vorhandene Anwendung von Direct3D 9 (d3d9) auf Direct3D 10 (d3d10) portieren soll.

-   [Konstantenpuffer](#constant-buffers)
-   [State](#state)
-   [Formate](#formats)
-   [Shaderverknüpfung](#shader-linkage)
-   [Draw-Aufrufe](#draw-calls)
-   [Ressourcen](#resources)
-   [Tiefe als Textur](#depth-as-texture)
-   [MSAA](#msaa)
-   [Abstürze](#crashes)
-   [Prädikat Rendering](#predicated-rendering)
-   [Geometrie-Shader](#geometry-shader)
-   [HLSL](#hlsl)

## <a name="constant-buffers"></a>Konstantenpuffer

<dl> <dt>

<span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>Was ist die beste Möglichkeit, Konstante Puffer zu aktualisieren?
</dt> <dd>

Updatesubresource und die Zuordnung mit verwerfen sollten ungefähr dieselbe Geschwindigkeit aufweisen. Wählen Sie zwischen diesen aus, je nachdem, welche Speichermenge den geringsten Speicherplatz kopiert. Wenn Ihre Daten bereits in einem zusammenhängenden Block im Speicher gespeichert sind, verwenden Sie updatesubresource. Wenn Sie Daten von anderen Orten sammeln müssen, verwenden Sie Map mit verwerfen.

</dd> <dt>

<span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>Was ist die schlechteste Methode zum Organisieren konstanter Puffer?
</dt> <dd>

Die schlechteste Leistung wird erzielt, indem alle Konstanten für einen bestimmten Shader in einen konstanten Puffer versetzt werden. Dies ist oft die einfachste Möglichkeit, von d3d9 zu d3d10 zu portieren. Dies kann jedoch die Leistung beeinträchtigen. Stellen Sie sich beispielsweise ein Szenario vor, in dem der folgende Konstante Puffer verwendet wird:

``` syntax
cbuffer VSGlobalsCB
{
    matrix  ViewProj;
    matrix  Bones[100];
    matrix  World;
    float   SpecPower;
    float4  BDRFCoefficients;
    float   AppTime;
    uint2   RenderTargetSize;
};
```

Der Puffer ist 6560 bytes. Angenommen, es gibt eine Anwendung mit 1000-Objekten, die gerendert werden sollen, 100 von den gehäuchten Meshes und 900, bei denen es sich um statische Netze handelt. Nehmen Sie außerdem an, dass diese Anwendung eine Schatten Zuordnung mit einer Lichtquelle verwendet. Dies bedeutet, dass es zwei Durchgänge gibt, eine für die Tiefe, die vom Licht gerendert wird, und eine für den Forward-Renderingdurchlauf. Dies führt zu 2000 Draw-aufrufen. Obwohl jeder zeichnen-Befehl nicht jeden Teil des Konstanten Puffers aktualisieren muss, wird der gesamte Konstante Puffer weiterhin aktualisiert und an die Karte gesendet. Dies führt zu einem Update von 13 MB Daten jedes Frames (2000 Draw-Aufrufe, 6560 KB).

</dd> <dt>

<span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>Was ist die beste Möglichkeit, meine Konstanten Puffer zu organisieren?
</dt> <dd>

Die beste Möglichkeit besteht darin, Konstante Puffer nach Aktualisierungshäufigkeit zu organisieren. Konstanten, die bei ähnlichen Frequenzen aktualisiert werden, müssen sich im gleichen Puffer befinden. Sehen Sie sich beispielsweise das Szenario an: "Was ist die schlechteste Methode zum Organisieren konstanter Puffer?", aber mit einem besseren Konstanten Layout:

``` syntax
cbuffer VSGlobalPerFrameCB
  { 
    float   AppTime; 
  };
cbuffer VSPerSkinnedCB
  { 
    matrix  Bones[100]; 
  };
cbuffer VSPerStaticCB
  {
    matrix  World;
  };
cbuffer VSPerPassCB
  {
    matrix  ViewProj;
    uint2   RenderTargetSize;
  };
cbuffer VSPerMaterialCB
  {
    float   SpecPower;
    float4  BDRFCoefficients;
  };    
```

Konstante Puffer werden nach ihrer Aktualisierungshäufigkeit aufgeteilt, aber dies ist nur die Hälfte der Lösung. Die Anwendung muss die Konstanten Puffer ordnungsgemäß aktualisieren, um die Aufteilung in vollem Umfang zu nutzen. Wir gehen von der gleichen Szene aus wie oben beschrieben: 900 statische Meshes, 100 häutige Meshes, ein heller Durchlauf und ein vorwärts Durchlauf. Außerdem wird davon ausgegangen, dass einige Konstante Puffer pro Objekt gespeichert werden. Dies bedeutet, dass jedes Objekt entweder ein vsperskinnedcb oder ein vsperstaticcb enthält, je nachdem, ob es ein-oder statisch ist. Dies geschieht, um zu vermeiden, dass die Anzahl der Matrizen, die über die Pipeline gesendet werden, verdoppelt wird.

Der Frame wird in drei Phasen aufgeteilt. Die erste Phase ist der Anfang des Frames und umfasst kein Rendering, sondern nur konstante Updates.

<dl> <dt>

<span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Anfangs Rahmen**
</dt> <dd>

-   Aktualisieren von vsglobalperframecb für die Anwendungszeit (4 Bytes)
-   Update 100 vsperskinnedcb für die 100 häutigen Objekte (640000 Bytes)
-   Vsperstaticcb für 900 statische Objekte aktualisieren (57600 Bytes)

Der nächste Schritt ist die schattenkarten Übergabe. Beachten Sie, dass der einzige Konstante Puffer, der tatsächlich aktualisiert wird, vsperpasscb ist. Alle anderen Konstanten Puffer wurden während der Übergabe des Frame Rahmens aktualisiert. Obwohl wir diese Konstanten Puffer immer noch binden müssen, ist die an die Grafikkarte weiter gegebene Informationsmenge minimal, da die Puffer bereits aktualisiert wurden.

</dd> <dt>

<span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Schatten Durchlauf**
</dt> <dd>

-   Vsperpasscb aktualisieren (72 Bytes)
-   Zeichnen Sie 100-Farb veräuchte Netze (100 Bindungen, keine Updates)
-   900 statische Netzen zeichnen (100 Bindungen, keine Updates)

Ebenso muss der Forward-Renderingdurchlauf nur die Daten pro Material aktualisieren, da Sie nicht pro Mesh gespeichert wurden. Wenn wir davon ausgehen, dass 500 Materialien in der Szene verwendet werden:

</dd> <dt>

<span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Forward-Durchlauf**
</dt> <dd>

-   Vsperpasscb aktualisieren (72 Bytes)
-   Update 500 vspermaterialcbs (10000 Bytes)

Dies ergibt insgesamt nur 707 KB. Obwohl es sich hierbei um ein sehr erfunantes Szenario handelt, wird veranschaulicht, wie sehr konstanter Aktualisierungs Aufwand durchsortieren von Konstanten nach Aktualisierungshäufigkeit reduziert werden kann.

</dd> </dl> </dd> <dt>

<span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>Was geschieht, wenn ich nicht genügend Speicherplatz zum Speichern einzelner konstanter Puffer für meine Netze, Materialien usw. habe? 
</dt> <dd>

Sie können immer ein mehrstufige System konstanter Puffer verwenden. Erstellen Sie Konstante Puffer variabler Größe (16 Bytes, 32 Bytes, 64 Bytes usw.) bis zur größten Konstanten Puffergröße. Wenn es an der Zeit ist, einen konstanten Puffer an einen Shader zu binden, wählen Sie den kleinsten Konstanten Puffer aus, der die vom Shader benötigten Daten enthalten kann. Obwohl dieser Ansatz etwas weniger effizient ist, ist dies ein guter Zwischenschritt.

</dd> <dt>

<span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>Ich gebe Konstante Puffer für verschiedene Shader frei. Ein Shader verwendet möglicherweise alle Konstanten, aber eine andere kann einige der Konstanten verwenden. Was ist die beste Möglichkeit, diese zu aktualisieren? 
</dt> <dd>

Ein Ansatz besteht darin, den konstanten Puffer noch weiter aufzuteilen. Es kommt jedoch zu einem Punkt, an dem zu viele Konstante Puffer gebunden sind. Verschieben Sie in diesem Fall die Konstanten, die von mehreren Shadern wahrscheinlich nicht verwendet werden, an das Ende des Konstanten Puffers. Wenn Sie die Variablen Daten aus dem Shader erhalten, verwenden Sie das d3d10 \_ SVF \_ used-Flag der d3d10 \_ Shader-Variablen, \_ \_ um zu bestimmen, ob die Variable verwendet wird. Wenn Sie nicht verwendete Variablen am Ende des Konstanten Puffers platzieren, können Sie einen kleineren Puffer an den Shader binden, der diese Variablen nicht verwendet, wodurch die Update Kosten eingespart werden.

</dd> <dt>

<span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>Wie viel kann ich meine Framerate verbessern, wenn ich meine Zeichen nur einmal pro Frame anstelle von einmal pro Durchlauf/zeichnen Auflade? 
</dt> <dd>

Abhängig von der Menge redundanter Daten können Sie die Framerate zwischen 8 Prozent und 50 Prozent verbessern. Im schlimmsten Fall wird die Leistung nicht reduziert.

</dd> <dt>

<span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>Wie viele Konstante Puffer sollte ich gleichzeitig gebunden haben? 
</dt> <dd>

Binden Sie die Mindestanzahl von konstantenpuffern, die benötigt wird, um alle Ihre Daten in den Shader zu übernehmen. In einem realistischen Szenario ist fünf die empfohlene Anzahl der zu verwendenden Konstanten Puffer. Durch die gemeinsame Verwendung konstanter Puffer zwischen Shader (die Bindung desselben CB an die vs und PS) kann auch die Leistung verbessert werden.

</dd> <dt>

<span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>Gibt es Kosten für das Binden konstanter Puffer, ohne Sie zu verwenden? 
</dt> <dd>

Ja, wenn Sie den Puffer nicht verwenden möchten, sollten Sie vssetconsantbuffer oder pssetconstantbuffer nicht aufrufen. Dieser zusätzliche API-Aufwand kann im Verlauf mehrerer Draw-Aufrufe entstehen.

</dd> </dl>

## <a name="state"></a>State

<dl> <dt>

<span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>Was ist die beste Möglichkeit, den Status in d3d10 zu verwalten? 
</dt> <dd>

Die beste Lösung besteht darin, den gesamten Zustand im Voraus zu kennen und die Zustands Objekte vorab zu erstellen. Dies bedeutet, dass zum Zeitpunkt der Rendering die Zustands Bindung der einzige Vorgang ist, der ausgeführt werden muss. D3d10 filtert auch Duplikate.

</dd> <dt>

<span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>Mein Spiel wurde dynamisch geladen oder verfügt über benutzergenerierten Inhalt. Ich kann nicht alle Zustands Objekte im Vordergrund laden.   Wie sollte ich vorgehen? 
</dt> <dd>

Hier gibt es zwei Lösungen. Der erste besteht darin, direkt Zustands Objekte zu erstellen und d3d10 das Herausfiltern von Duplikaten zu ermöglichen. Dies wird jedoch nicht für Szenarien mit vielen Zustands Objektänderungen pro Frame empfohlen. Eine bessere Lösung besteht darin, die Zustands Objekte selbst zu Hashen und nur dann ein Zustands Objekt zu erstellen, wenn ein Objekt, das den Anforderungen entspricht, nicht in der Hash Tabelle gefunden wird. Wenn eine benutzerdefinierte Hash Tabelle verwendet wird, kann eine Anwendung einen schnellen Hash basierend auf dem Anwendungsszenario auswählen, das speziell für diese Anwendung gilt. Wenn eine Anwendung z. b. nur rendertargetschreitemask im blendstate ändert und alle anderen Werte identisch ist, kann die Anwendung einen Hash aus rendertargetschreitemask anstelle der gesamten Struktur generieren.

</dd> <dt>

<span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>Der Alpha-Atest Zustand ist nicht mehr vorhanden. Wo war es? 
</dt> <dd>

Alpha Atest sollte jetzt im Shader Leistung aufweisen. Weitere Informationen finden Sie unter fixedfuncemu Sample.

</dd> <dt>

<span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>Was ist mit Benutzer Clip-Flächen passiert? 
</dt> <dd>

Benutzer Clip Flächen wurden in den Shader verschoben. Hierfür gibt es zwei Möglichkeiten. Der erste Wert ist die Ausgabe \_ von SV clipdistance aus dem Vertex-Shader oder dem Geometry-Shader. Die andere Option ist die Verwendung von verwerfen im Pixelshader basierend auf einem Wert, der vom Vertex-Shader oder dem Geometry-Shader nach unten übermittelt wird. Experimentieren Sie mit beiden, um zu sehen, was für ihr bestimmtes Szenario schneller ist. Die Verwendung \_ von SV clipdistance könnte dazu führen, dass die Hardware eine Geometrie basierte clippingroutine verwendet, die dazu führen kann, dass Geometrie gebundene Draw-Aufrufe langsamer ausgeführt werden. Ebenso verlagert die Verwendung von verwerfen die Arbeit in den Pixelshader, was dazu führen kann, dass Pixel gebundene Draw-Aufrufe langsamer ausgeführt werden.

</dd> <dt>

<span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Bei der Löschung werden keine Zustands Einstellungen berücksichtigt, wie z. b. die Einstellungen für den Scheren-Rect in My Rasterizer State. 
</dt> <dd>

Das Löschen wurde vom Pipeline Status getrennt. Um das Verhalten von d3d9 zu erhalten, emulieren Sie die Löschung durch Zeichnen eines voll Bild Quad.

</dd> <dt>

<span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>Ich habe meine Zustände wieder auf den Standardwert festgelegt, um einen Renderingfehler zu diagnostizieren. Mein Bildschirm zeigt nur schwarz an, obwohl ich weiß, dass Objekte auf dem Bildschirm gezeichnet werden. 
</dt> <dd>

Stellen Sie beim Festlegen des Zustands zurück auf die Standardwerte (null) sicher, dass die samplemask im Befehl omsetblendstate niemals 0 (null) ist. Wenn samplemask auf 0 (null) festgelegt ist, werden alle Beispiele logisch und mit 0 (null). In diesem Szenario bestehen keine Beispiele für den Blend-Test.

</dd> <dt>

<span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Wo liegt der D3DSAMP \_ srgbtexture-Status? 
</dt> <dd>

SRGB wurde als Teil des samplingzustands entfernt und ist nun an das Textur Format gebunden. Das Binden einer sRGB-Textur führt zu derselben Stichprobe, die Sie erhalten, wenn Sie D3DSAMP \_ srgbtexture in Direct3D 9 angegeben haben.

</dd> </dl>

## <a name="formats"></a>Formate

<dl> <dt>

<span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Welches d3d9-Format entspricht dem d3d10-Format? 
</dt> <dd>

Weitere Informationen finden [Sie unter Direct3D 9 to Direct3D 10 Überlegungen](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).

</dd> <dt>

<span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>Was ist mit A8R8G8B8-Textur Formaten passiert? 
</dt> <dd>

Sie wurden in d3d10 als veraltet markiert. Sie können Ihre Texturen als R8G8B8A8 wieder verwenden, oder Sie können auf die Last ziehen, oder Sie können den Shader in den Shader ziehen.

</dd> <dt>

<span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>Gewusst wie die Verwendung von Paletten-Texturen? 
</dt> <dd>

Platzieren Sie die Farbpalette in einer Textur oder einem konstanten Puffer, und binden Sie Sie an die Pipeline. Führen Sie im Pixel-Shader eine indirekte Suche mithilfe des Indexes in der in der paletbasierten Textur aus.

</dd> <dt>

<span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>Welche neuen sRGB-Formate sind verfügbar? 
</dt> <dd>

SRGB wurde als Teil des samplingzustands entfernt und ist nun an das Textur Format gebunden. Das Binden einer sRGB-Textur führt zu derselben Stichprobe, die Sie erhalten, wenn Sie D3DSAMP \_ srgbtexture in Direct3D 9 angegeben haben.

</dd> <dt>

<span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Wo sind die Dreiecks Fans unterwegs? 
</dt> <dd>

Dreiecks Fans wurden in d3d10 als veraltet markiert. Dreiecks Lüfter müssen entweder in der Inhalts Pipeline oder beim Laden konvertiert werden.

</dd> </dl>

## <a name="shader-linkage"></a>Shaderverknüpfung

<dl> <dt>

<span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>Meine Direct3D 9-Shader werden problemlos in Shader-Modell 4,0 kompiliert, aber wenn ich Sie an die Pipeline bindet, erhalte ich Verknüpfungs Fehler, die in der Debug-Ausgabe mit der Debug-Laufzeit angezeigt werden. 
</dt> <dd>

Die Shader-Verknüpfung ist in d3d10 wesentlich strenger. Elemente in einer nachfolgenden Phase müssen in der Reihenfolge gelesen werden, in der Sie aus der vorherigen Phase ausgegeben werden. Beispiel:

Vertex-Shader-Ausgaben:

``` syntax
    float4 Pos  : SV_POSITION;
    float3 Norm : NORMAL;
    float2 Tex  : TEXCOORD0;
```

Ein Pixelshader liest in:

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

Obwohl die Position im Pixelshader nicht benötigt wird, verursacht dies einen Verknüpfungs Fehler, da die Position vom Vertexshader ausgegeben, aber nicht vom Pixelshader gelesen wird. Die korrekte Version sieht wie folgt aus:

Vertex-Shader-Ausgaben:

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
        float4 Pos  : SV_POSITION;
```

Ein Pixelshader liest in:

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

In diesem Fall gibt der Vertex-Shader die gleichen Informationen aus, aber jetzt liest der Pixelshader Dinge in der Auftrags Ausgabe. Da der Pixelshader nichts nach TeX liest, müssen wir uns keine Sorgen machen, dass vs mehr Informationen ausstellt, als das PS liest.

</dd> <dt>

<span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>Ich benötige eine shadersignatur, um ein Eingabe Layout zu erstellen, aber ich lade meine Netze und erstelle Layouts vor dem Erstellen von Shadern. Wie gehe ich vor? 
</dt> <dd>

Eine Lösung besteht darin, die Reihenfolge zu wechseln und Shader vor dem Laden von Netzen zu laden. Dies ist jedoch viel einfacher zu tun als durchgeführt. Sie können die Eingabe Layouts immer bei Bedarf erstellen, wenn Sie von der Anwendung benötigt werden. Sie müssen eine Version der shadersignatur aufbewahren. Sie sollten einen Hash erstellen, der auf dem Shader und dem Puffer Layout basiert, und das Eingabe Layout nur dann erstellen, wenn eine Übereinstimmung vorhanden ist, die noch nicht vorhanden ist.

</dd> </dl>

## <a name="draw-calls"></a>Draw-Aufrufe

<dl> <dt>

<span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>Was ist meine Beschränkung für Draw-Aufrufe für d3d10, um 60 Hz zu erreichen? 30 Hz? 
</dt> <dd>

Bei Direct3D 9 ist aufgrund der CPU-Kosten pro Draw-Aufruf eine Beschränkung für die Anzahl der Draw-Aufrufe aufgetreten. Auf Direct3D 10 wurden die Kosten für jeden zeichnen-Befehl reduziert. Es gibt jedoch keine eindeutige Korrelation zwischen Draw-aufrufen und Frameraten. Da Draw-Aufrufe häufig viele Support Aufrufe erfordern (Konstante Puffer Aktualisierungen, Textur Bindungen, Zustands Einstellungen usw.), sind die Auswirkungen der-API auf die Frame Rate jetzt eher von der allgemeinen API-Nutzung abhängig, anstatt durch Zeichnen von Ansichts Anzahlen.

</dd> </dl>

## <a name="resources"></a>Ressourcen

<dl> <dt>

<span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>Welchen Ressourcen Verwendungstyp sollte ich für welche Vorgänge verwenden? 
</dt> <dd>

Verwenden Sie das folgende Spick Blatt:

-   Die CPU aktualisiert die Ressource mehrmals pro Frame: d3d10 \_ Usage \_ Dynamic
-   Die CPU aktualisiert die Ressource weniger als einmal pro Frame: d3d10 \_ Usage \_ default
-   Die CPU aktualisiert nicht die Ressource: d3d10 \_ Usage \_ unveränderlich
-   Die CPU muss die Ressource lesen: d3d10 \_ Usage \_ Staging

Da Konstante Puffer immer häufig aktualisiert werden sollen, entsprechen Sie nicht dem "Cheat Sheet". Informationen zu den Ressourcentypen, die für konstante Puffer verwendet werden sollen, finden Sie im Abschnitt [Konstantenpuffer](#constant-buffers) .

</dd> <dt>

<span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>Was ist mit drawprimitiveup und drawindexedprimitiveup passiert? 
</dt> <dd>

Sie sind in d3d10 nicht mehr vorhanden. Verwenden Sie für Dynamic geometry einen dynamischen Puffer mit hoher d3d10- \_ Verwendung \_ . Ordnen Sie ihn am Anfang des Frames der d3d10 Map- \_ \_ Schreib \_ Verwerfungs zu. Bei jedem nachfolgenden Draw-Befehl sollte der Schreib Zeiger über die Position der zuvor gezeichneten Scheitel Punkte hinausgezogen werden, und der Puffer wird mit d3d10 \_ map \_ Write \_ No überschrieben zugeordnet \_ . Wenn Sie sich am Ende des Puffers vor dem Ende des Frames befinden, umschließen Sie den Schreib Zeiger um den Anfang und die Zuordnung mit d3d10 \_ map \_ Write \_ verwerfen.

</dd> <dt>

<span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>Kann ich 16-Bit-Indizes und 32-Bit-Indizes in denselben dynamischen Geometry-Puffer schreiben? 
</dt> <dd>

Ja, das ist möglich, aber dies kann zu einer Leistungs Einbuße auf bestimmter Hardware werden. Es ist sicherer, separate Puffer für dynamische 16-Bit-Indexdaten und 32-Bit-Indexdaten zu erstellen.

</dd> <dt>

<span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>Gewusst wie Daten von der GPU auf die CPU zurück lesen? 
</dt> <dd>

Sie müssen eine Staging-Ressource verwenden. Kopieren Sie die Daten aus der GPU-Ressource mithilfe von copyresource in die stagingressource. Ordnen Sie die stagingressource zu, um die Daten zu lesen.

</dd> <dt>

<span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>Meine Anwendung war von der stretchrect-Funktion abhängig. 
</dt> <dd>

Da es sich im Wesentlichen um einen Wrapper für grundlegende Direct3D-Funktionen handelt, wurde er aus der API entfernt. Einige der stretchrect-Funktionen wurden in D3DX10LoadTextureFromTexture verschoben. Für Formatkonvertierungen und das Kopieren von Texturen kann D3DX10LoadTextureFromTexture den Auftrag ausführen. Vorgänge, wie z. b. die Umstellung von einer Größe in eine andere, erfordern jedoch in der Anwendung einen Rendering-zu-Textur-Vorgang.

</dd> <dt>

<span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>Es gibt keine Offsets oder Größen für Zuordnungs Aufrufe für Ressourcen. Diese waren bei Sperr aufrufen auf Direct3D 9 vorhanden. Warum haben Sie sich geändert? 
</dt> <dd>

Die Offsets und Größen für Sperr Aufrufe auf Direct3D 9 waren im Grunde genommen API-Übersichtlichkeit und werden oft vom Treiber ignoriert. Offsets sollten stattdessen von der Anwendung aus dem im Map-Befehl zurückgegebenen Zeiger berechnet werden.

</dd> </dl>

## <a name="depth-as-texture"></a>Tiefe als Textur

<dl> <dt>

<span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Was ist schneller? Sie verwenden Tiefe als Textur oder schreiben Tiefe in Alpha und lesen diese? 
</dt> <dd>

Dabei handelt es sich um Anwendungs-und Hardware spezifische Anwendungen. Verwenden Sie, je nachdem, welche Bandbreite eingespart wird. Wenn Sie bereits mehrere Renderziele verwenden und über einen zusätzlichen Kanal verfügen, ist das Schreiben von Tiefe aus dem Shader möglicherweise eine bessere Lösung. Außerdem können Sie mit dem Schreiben von Tiefe in Alpha oder einem anderen Renderziel lineare tiefen Werte schreiben, mit denen Berechnungen beschleunigt werden können, die auf den tiefen Puffer zugreifen müssen.

</dd> <dt>

<span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>Kann eine Textur als Eingabe gebunden und als Tiefe der tiefen Schablone gebunden werden, solange ich die Tiefe von Schreibvorgängen deaktiviere? 
</dt> <dd>

Nicht in d3d10.

</dd> </dl>

## <a name="msaa"></a>MSAA

<dl> <dt>

<span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>Kann ich eine MSAA-tiefen Schablone auflösen? 
</dt> <dd>

Nicht in d3d10. Allerdings können Sie Stichproben einzelner Beispiele aus der MSAA-Textur durch sehen. Weitere Informationen finden Sie im Abschnitt [HLSL](#hlsl) .

</dd> <dt>

<span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Warum stürzt meine Anwendung ab, sobald ich MSAA aktiviere? 
</dt> <dd>

Stellen Sie sicher, dass Sie eine MSAA-Stichproben Anzahl und eine Qualitäts Nummer aktivieren, die tatsächlich vom Treiber aufgelistet werden.

</dd> </dl>

## <a name="crashes"></a>Abstürze

<dl> <dt>

<span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>Meine Anwendung stürzt in d3d10 oder im Treiber ab, und ich weiß nicht, warum dies der Fall ist. 
</dt> <dd>

Der erste Schritt besteht darin, die Debug-Laufzeit zu aktivieren ([**d3d10 \_ Create \_ Device \_ Debug**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) Flag an [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)). Dadurch werden die häufigsten Fehler als Debugausgaben angezeigt.

</dd> <dt>

<span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>Pix stürzt ab, wenn ich versuche, meine Anwendung mit der Anwendung zu verwenden. 
</dt> <dd>

Der erste Schritt besteht darin, die Debug-Laufzeit zu aktivieren ([**d3d10 \_ Create \_ Device \_ Debug**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) Flag an [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)). Pix hat eine viel höhere Wahrscheinlichkeit, dass ein Absturz erfolgt, wenn die Debugausgabe nicht bereinigt ist.

</dd> <dt>

<span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>Mein Spiel läuft auf dem 32-Bit-Vista unter d3d10 auf dem virtuellen Adressraum. Auf d3d9 sind keine Probleme aufgetreten. 
</dt> <dd>

Bei d3d10 und dem virtuellen Adressraum sind einige Probleme aufgetreten. Dies wurde in [KB940105](https://support.microsoft.com/kb/940105)behoben. Wenn das Problem nicht behoben wird, stellen Sie sicher, dass Sie nicht mehr Ressourcen erstellen, die in d3d10 zugeordnet werden können, als Sie in d3d9 erstellt haben. Stellen Sie sich auch die Portierung auf 64-Bit vor, da dies in Zukunft häufiger wird.

</dd> </dl>

## <a name="predicated-rendering"></a>Prädikat Rendering

<dl> <dt>

<span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>Ich habe ein Prädikat Rendering verwendet (basierend auf den Ergebnissen der Okklusions Abfrage). Warum wird meine APP immer noch dieselbe Geschwindigkeit haben? 
</dt> <dd>

Stellen Sie zunächst sicher, dass das Rendering, das Sie überspringen möchten, tatsächlich der Anwendungs Engpass ist. Wenn dies nicht der Engpass ist, wird beim Überspringen des Renderings nicht die Framerate unterstützt.

Stellen Sie außerdem sicher, dass zwischen dem Problem der Abfrage und dem Rendering, das Sie als Prädikat festlegen möchten, genügend Zeit vergangen ist. Wenn die Abfrage nicht durch den Zeitpunkt abgeschlossen ist, zu dem der renderingaufruf auf die GPU trifft, wird das Rendering trotzdem durchzuführen.

Drittens überspringt das Prädikat nur bestimmte Aufrufe. Die übersprungenen Aufrufe sind Draw, Clear, Copy, Update, resolvesubresource und generatemips. Die Zustands Einstellung, IA-Setup, Map und Create-Aufrufe berücksichtigen das Prädikat nicht. Wenn eine Menge von Zustands Einstellungs aufrufen für den Draw-Aufruf vorhanden ist, die als Prädikat verwendet werden sollen, werden diese Zustände weiterhin festgelegt.

</dd> </dl>

## <a name="geometry-shader"></a>Geometrie-Shader

<dl> <dt>

<span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Sollte ich den Geometry-Shader verwenden, um "My" zu Mosaik (hier einfügen)? 
</dt> <dd>

Nein. Der Geometry-Shader sollte nicht für Mosaik verwendet werden.

</dd> <dt>

<span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>Kann ich den Geometry-Shader zum Erstellen von Geometrie verwenden? 
</dt> <dd>

Ja, in sehr begrenzten Szenarios. Der Geometry-Shader in aktuellen d3d10 (2008) teilen ist nicht für die Verarbeitung einer großen Erweiterung zuständig. Dies kann sich in Zukunft ändern. Bei Video Karten Anbietern gibt es möglicherweise einen speziellen Pfad für einen bis vier Erweiterungen, weil Sie über eine vorhandene Hardware verfügen. Alle anderen Erweiterungen müssten sehr eingeschränkt sein. Die Beispiele "particlesgs" und "pipesgs" erzielen hohe Frameraten, da nur eine begrenzte Erweiterung durchgeführt wird. Pro Frame werden nur einige Punkte erweitert.

</dd> <dt>

<span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>Wofür sollte ich den Geometry-Shader verwenden? 
</dt> <dd>

Alles, was Vorgänge für einen ganzen primitiven erfordert, wie z. b. die Silhouette-Erkennung, baryzentrische Koordinaten usw. Verwenden Sie diese Option auch zum Auswählen des Slice eines renderzielarrays, an das primitive gesendet werden sollen.

</dd> <dt>

<span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>Kann ich Variablen Mengen von Geometrie aus dem Geometry-Shader ausgeben? 
</dt> <dd>

Ja, dies kann jedoch zu Leistungsproblemen führen. Betrachten Sie das Beispiel für die Ausgabe von 1 Punkt für einen Aufruf und 4 Punkte für einen anderen. Bei der Anpassung innerhalb der Erweiterungs Richtlinien kann dies dazu führen, dass die Geometry-Shader-Threads serialisiert ausgeführt werden.

</dd> <dt>

<span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>Wie kann d3d10 wissen, wie Sie die einstellungsindizes für mein Mesh generieren? Oder warum wird d3d10 nicht ordnungsgemäß Rendering, wenn angegeben wird, dass der Geometry-Shader Informationen zu Informationen benötigt. 
</dt> <dd>

Die Informationen zu den Informationen werden nicht von d3d10, sondern von der Anwendung erstellt. Die Indikations Indizes werden von der Anwendung generiert und müssen sechs Indizes pro primitiver Zeichen enthalten. die sechs nummerierten Indizes sind die Rand angrenzenden Vertices. ID3DX10Mesh:: generatezuruencyandpoinzreps kann verwendet werden, um diese Daten zu generieren.

</dd> </dl>

## <a name="hlsl"></a>HLSL

<dl> <dt>

<span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Sind ganzzahlige und bitweise Anweisungen langsam? 
</dt> <dd>

Sie können sein. Verschiedene d3d10-Karten können nur ganzzahlige Vorgänge für eine Teilmenge der verfügbaren Alu-Einheiten ausgeben. Dies hängt stark von der Hardware ab. Empfehlungen zum Umgang mit ganz Zahl Vorgängen auf der jeweiligen Hardware finden Sie unter Hardwarehersteller. Seien Sie außerdem sehr vorsichtig bei Umwandlungen zwischen Typen.

</dd> <dt>

<span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>Was ist mit vpos passiert? 
</dt> <dd>

Wenn Sie eine Eingabe für den Pixelshader als SV- \_ Position deklarieren, erhalten Sie das gleiche Verhalten wie beim Deklarieren als vpos.

</dd> <dt>

<span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>Gewusst wie Beispiel für eine MSAA-Textur? 
</dt> <dd>

Deklarieren Sie die Textur im Shader als Texture2DMS. Anschließend können Sie einzelne Beispiele mithilfe der Beispiel Methoden aus dem Texture2DMS-Objekt abrufen.

</dd> <dt>

<span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>Gewusst wie erkennen, ob eine Shader-Variable in einem konstanten Puffer tatsächlich verwendet wird? 
</dt> <dd>

Sehen Sie sich die reflektierte d3d10 \_ Shader Variable Debug- \_ \_ Struktur für diese Variable an. für uFlags sollte das \_ verwendete Flag d3d10 SVF \_ festgelegt sein.

</dd> <dt>

<span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>Gewusst wie erkennen, ob eine Shader-Variable in einem konstanten Puffer tatsächlich FX10 verwendet? 
</dt> <dd>

Dies ist derzeit nicht möglich, wenn Sie FX10 verwenden.

</dd> <dt>

<span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>Ich habe keine Kontrolle über die Konstanten Puffer, die von FX10 erstellt werden. Wie werden Sie erstellt und aktualisiert? 
</dt> <dd>

Alle FX10-verwalteten Konstanten Puffer werden als Standard Ressourcen für die d3d10 \_ -Verwendung erstellt \_ und mithilfe von updatesubresource aktualisiert. Da FX10 einen Sicherungs Speicher für alle Konstanten Daten beibehält, ist updatesubresource der beste Ansatz zum Aktualisieren dieser Daten.

</dd> <dt>

<span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>Gewusst wie die Pipeline mit der Fixed-Funktion mithilfe von Shadern emulieren? 
</dt> <dd>

Siehe fixedfuncemu Sample.

</dd> <dt>

<span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>Sollten die neuen \[ \] \[ \] \[ compilerhinweise "auflösen", "Loop", "Branch" usw. verwendet \] werden? 
</dt> <dd>

Im Allgemeinen nicht. Der Compiler versucht häufig, beide Methoden zu verwenden und den schnellsten auszuwählen. In einigen Fällen ist es möglicherweise erforderlich, die Registrierung zu verwenden \[ \] , z. b. Wenn ein Textur Abruf innerhalb einer Schleife Zugriff auf einen Farbverlauf benötigt.

</dd> <dt>

<span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>Nimmt die partielle Genauigkeit einen Unterschied zu d3d10? Ich kann eine partielle Genauigkeit in My d3d9 HLSL angeben, jedoch nicht in My d3d10 HLSL. 
</dt> <dd>

Alle d3d10-Vorgänge werden für die Ausführung mit einer Gleit Komma Genauigkeit von 32 Bit angegeben. Daher sollte die partielle Genauigkeit keinen Unterschied in d3d10 haben.

</dd> <dt>

<span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>In d3d9 könnte ich eine HW-PCF-Schatten Filterung durchführen, indem ich einen tiefen Puffer als Textur bindet und reguläre tex2d HLSL-Anweisungen verwende. Gewusst wie dies auf d3d10? 
</dt> <dd>

Sie müssen einen Vergleichs samplerstatus verwenden und samplecmp-Anweisungen verwenden.

</dd> <dt>

<span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>Wie funktioniert dieses Registrierungs Schlüsselwort in d3d10? 
</dt> <dd>

Das Register-Schlüsselwort in d3d10 gilt nun für den Slot, an den eine bestimmte Ressource gebunden ist. In diesem Fall kann die Ressource ein Puffer (konstant oder anderweitig), eine Textur oder ein Sampler sein.

-   Verwenden Sie für konstante Puffer die Syntax: Register (bN), wobei N der Eingabe Slot (0-15) ist.
-   Verwenden Sie für Texturen die Syntax: Register (tN), wobei N der Eingabe Slot (0-127) ist.
-   Verwenden Sie für Samplers die Syntax: Register (SN), wobei N der Eingabe Slot (0-127) ist.

</dd> <dt>

<span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>Gewusst wie eine Variable innerhalb eines konstanten Puffers platzieren, wenn "Register" nur verwendet wird, um anzugeben, wo der gesamte Puffer gebunden werden soll? 
</dt> <dd>

Verwenden Sie das packoffset-Schlüsselwort. Das Argument für packoffset hat das Format c \[ 0-4095 \] . \[ x, y, z, w \] . Beispiel:

``` syntax
        cbuffer cbLotsOfEmptySpace
        {
        float   IWaste2Floats   : packoffset(c0.z);
        float4  IWasteMore  : packoffset(c13);
        };
```

In diesem Konstanten Puffer wird IWaste2Floats bei der dritten Gleit Komma Zahl (12. Byte) im Konstanten Puffer platziert. Iwastemore wird am 13. float4 oder 52nd im Konstanten Puffer platziert.

</dd> </dl>

 

 