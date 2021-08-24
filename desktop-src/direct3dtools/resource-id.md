---
description: Definiert Ressourcen-IDs für freigegebene Zeichenfolgenressourcen.
MS-HAID: vspixengine.Resource\_Id
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Resource_Id-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC04FDC4-CD35-4A87-8EE8-48FFA07B8FC0
api_name:
- Resource_Id
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c0652796061b7875bca068bf72d53da541b941518990b4616ae1d1948c0d3e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787970"
---
# <a name="span-idvspixengineresource_idspanresource_id-enumeration"></a><span id="vspixengine.resource_id"></span>\_Ressourcen-ID-Enumeration

Definiert Ressourcen-IDs für freigegebene Zeichenfolgenressourcen. Diese werden vom Host an die Erfassungs-Engine übergeben. Sie werden verwendet, um Zeichenfolgen in der HUD-Überlagerung der erfassten App anzuzeigen oder Registrierungswerte von Visual Studio Optionen an die Erfassungs-ENGI zu übergeben.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="IDS_ENGINEDISCONNECTED"></span><span id="ids_enginedisconnected"></span>**\_IDS-ENGINEDISCONNECTED**  
Wird nicht verwendet. Ressourcen-ID für zeichenfolge, die zuvor verwendet wurde, um anzugeben, dass der Druckbildschirm nach Abschluss der Aufzeichnungssitzung erreicht wurde.

<span id="IDR_RCDATA1"></span><span id="idr_rcdata1"></span>**IDR \_ RCDATA1**  
Wird nicht verwendet.

<span id="IDS_DEFAULTEXPFILE_CONTENT"></span><span id="ids_defaultexpfile_content"></span>**IDS \_ \_ DEFAULTEXPFILE-INHALT**  
Wird nicht verwendet. Ressourcen-ID für Zeichenfolge, die früher für XML-Daten in Legacyerfassungsszenarien verwendet wurde.

<span id="IDS_CAPTURE_MESSAGE"></span><span id="ids_capture_message"></span>**IDS \_ CAPTURE \_ MESSAGE**  
Ressourcen-ID für die Zeichenfolge "Erfasster Frame".

<span id="IDS_CAPTURE_NOT_SUPPORTED"></span><span id="ids_capture_not_supported"></span>**IDS \_ CAPTURE \_ NICHT \_ UNTERSTÜTZT**  
Ressourcen-ID für die Zeichenfolge "Dieses Programm hat angegeben, dass es nicht mit Grafikdiagnose Tools verwendet werden kann."

<span id="IDS_CAPTURE_NOT_SUPPORTED_TITLE"></span><span id="ids_capture_not_supported_title"></span>**IDS \_ CAPTURE \_ NOT \_ SUPPORTED \_ TITLE**  
Ressourcen-ID für die Zeichenfolge "Nicht unterstützte Funktionalität"

<span id="IDS_FEATURE_NOT_SUPPORTED"></span><span id="ids_feature_not_supported"></span>**\_IDS-FEATURE \_ WIRD NICHT \_ UNTERSTÜTZT**  
Ressourcen-ID für die Zeichenfolge "Gerätefunktionsebene wird nicht unterstützt"

<span id="IDS_DXVERSION_NOT_SUPPORTED"></span><span id="ids_dxversion_not_supported"></span>**IDS \_ DXVERSION \_ WIRD NICHT \_ UNTERSTÜTZT**  
Ressourcen-ID für die Zeichenfolge "DirectX-Version kann nicht erfasst werden"

<span id="IDS_DCOMP_NOT_SUPPORTED"></span><span id="ids_dcomp_not_supported"></span>**IDS \_ DCOMP \_ NICHT \_ UNTERSTÜTZT**  
Ressourcen-ID für die Zeichenfolge "DCOMP wird von der App verwendet, aber unter diesem Betriebssystem nicht unterstützt"

<span id="IDS_DWRITE_NOT_SUPPORTED"></span><span id="ids_dwrite_not_supported"></span>**IDS \_ DWRITE \_ WIRD NICHT \_ UNTERSTÜTZT**  
Ressourcen-ID für die Zeichenfolge "DWRITE wird von der App verwendet, wird aber unter diesem Betriebssystem nicht unterstützt"

<span id="IDS_EXPECTED_FAILURE_FORMAT"></span><span id="ids_expected_failure_format"></span>**IDS \_ EXPECTED \_ FAILURE \_ FORMAT**  
Ressourcen-ID für die Zeichenfolge "%s hat während der Wiedergabe einen Fehler zurückgegeben. (HRESULT=%s) \\ r \\ n".

<span id="IDS_CAPTURETOOLTIP_MESSAGE"></span><span id="ids_capturetooltip_message"></span>**IDS \_ CAPTURETOOLTIP \_ MESSAGE**  
Ressourcen-ID für die Zeichenfolge "Verwenden Sie die Taste "Druckbildschirm", um einen Frame zu erfassen."

<span id="IDS_D2D_AND_D10_NOT_SUPPORTED"></span><span id="ids_d2d_and_d10_not_supported"></span>**IDS \_ D2D \_ UND \_ D10 \_ WERDEN NICHT \_ UNTERSTÜTZT**  
Ressourcen-ID für die Zeichenfolge "D2D und D10 werden unter diesem Betriebssystem nicht zusammen unterstützt"

<span id="IDS_HUD_STATISTICS"></span><span id="ids_hud_statistics"></span>**IDS \_ HUD \_ STATISTICS**  
Ressourcen-ID für zeichenfolge "Frames captured %d. Framezeit (ms) %0,00f"

<span id="IDS_INTERNAL_METHOD"></span><span id="ids_internal_method"></span>**INTERNE \_ \_ IDS-METHODE**  
Ressourcen-ID für die Zeichenfolge "Directx Internal Method"

<span id="IDS_CAPTURE_FRAME_MARK"></span><span id="ids_capture_frame_mark"></span>**IDS \_ CAPTURE \_ FRAME \_ MARK**  
Ressourcen-ID für die Zeichenfolge "Captured Frame %ld"

<span id="PIPELINESTAGE_INPUTASSEMBLER"></span><span id="pipelinestage_inputassembler"></span>**PIPELINESTAGE \_ INPUTASSEMBLER**  
Wird nicht verwendet.

<span id="PIPELINESTAGE_VERTEXSHADER"></span><span id="pipelinestage_vertexshader"></span>**PIPELINESTAGE \_ VERTEXSHADER**  
Wird nicht verwendet.

<span id="PIPELINESTAGE_HULLSHADER"></span><span id="pipelinestage_hullshader"></span>**PIPELINESTAGE \_ HULLSHADER**  
Wird nicht verwendet.

<span id="PIPELINESTAGE_TESSELATOR"></span><span id="pipelinestage_tesselator"></span>**\_PIPELINESTAGE-TESSELATOR**  
Wird nicht verwendet.

<span id="PIPELINESTAGE_DOMAINSHADER"></span><span id="pipelinestage_domainshader"></span>**PIPELINESTAGE \_ DOMAINSHADER**  
Wird nicht verwendet.

<span id="PIPELINESTAGE_GEOMETRYSHADER"></span><span id="pipelinestage_geometryshader"></span>**PIPELINESTAGE \_ GEOMETRYSHADER**  
Wird nicht verwendet.

<span id="PIPELINESTAGE_STREAMOUTPUT"></span><span id="pipelinestage_streamoutput"></span>**PIPELINESTAGE \_ STREAMOUTPUT**  
Wird nicht verwendet.

<span id="PIPELINESTAGE_RASTERIZER"></span><span id="pipelinestage_rasterizer"></span>**\_PIPELINESTAGE-RASTERIZER**  
Wird nicht verwendet.

<span id="PIPELINESTAGE_PIXELSHADER"></span><span id="pipelinestage_pixelshader"></span>**PIPELINESTAGE \_ PIXELSHADER**  
Wird nicht verwendet.

<span id="PIPELINESTAGE_OUTPUTMERGER"></span><span id="pipelinestage_outputmerger"></span>**PIPELINESTAGE \_ OUTPUTMERGER**  
Wird nicht verwendet.

<span id="PIPELINESTAGE_COMPUTESHADER"></span><span id="pipelinestage_computeshader"></span>**PIPELINESTAGE \_ COMPUTESHADER**  
Wird nicht verwendet.

<span id="BUFFEROBJECT_SUPPORTEDFORMAT"></span><span id="bufferobject_supportedformat"></span>**BUFFEROBJECT \_ SUPPORTEDFORMAT**  
Wird nicht verwendet.

<span id="BUFFEROBJECT_CURRENTFORMAT"></span><span id="bufferobject_currentformat"></span>**BUFFEROBJECT \_ CURRENTFORMAT**  
Wird nicht verwendet.

<span id="BUFFEROBJECT_HEADER"></span><span id="bufferobject_header"></span>**\_BUFFEROBJECT-HEADER**  
Wird nicht verwendet.

<span id="BUFFEROBJECT_LINE"></span><span id="bufferobject_line"></span>**BUFFEROBJECT \_ LINE**  
Wird nicht verwendet.

<span id="BUFFEROBJECT_INVALIDFORMAT"></span><span id="bufferobject_invalidformat"></span>**BUFFEROBJECT \_ INVALIDFORMAT**  
Wird nicht verwendet.

<span id="BUFFEROBJECT_INVALIDEMPTYFORMAT"></span><span id="bufferobject_invalidemptyformat"></span>**BUFFEROBJECT \_ INVALIDEMPTYFORMAT**  
Wird nicht verwendet.

<span id="BUFFEROBJECT_INVALIDFORMATSIZE"></span><span id="bufferobject_invalidformatsize"></span>**BUFFEROBJECT \_ INVALIDFORMATSIZE**  
Wird nicht verwendet.

<span id="SUMMARYINFO_TARGETAPPLICATION"></span><span id="summaryinfo_targetapplication"></span>**SUMMARYINFO \_ TARGETAPPLICATION**  
Im Vsglog-Eigenschaftenfenster angezeigter Text – Zielanwendung

<span id="SUMMARYINFO_PATH"></span><span id="summaryinfo_path"></span>**\_SUMMARYINFO-PFAD**  
Im vsglog-Eigenschaftenfenster angezeigter Text – Pfad

<span id="SUMMARYINFO_TARGETVERSION"></span><span id="summaryinfo_targetversion"></span>**SUMMARYINFO \_ TARGETVERSION**  
Im vsglog-Eigenschaftenfenster – Zielversion angezeigter Text

<span id="SUMMARYINFO_LASTMODIFIEDDATE"></span><span id="summaryinfo_lastmodifieddate"></span>**SUMMARYINFO \_ LASTMODIFIEDDATE**  
Im vsglog-Eigenschaftenfenster angezeigter Text – Datum der letzten Änderung

<span id="SUMMARYINFO_PROCESSID"></span><span id="summaryinfo_processid"></span>**SUMMARYINFO \_ PROCESSID**  
Im vsglog-Eigenschaftenfenster – Prozess-ID angezeigter Text

<span id="SUMMARYINFO_EXPERIMENTFILE"></span><span id="summaryinfo_experimentfile"></span>**SUMMARYINFO \_ EXPERIMENTFILE**  
Im vsglog-Eigenschaftenfenster – Experimentdatei angezeigter Text

<span id="SUMMARYINFO_RUNFILE"></span><span id="summaryinfo_runfile"></span>**SUMMARYINFO \_ RUNFILE**  
Im vsglog-Eigenschaftenfenster – Datei ausführen angezeigter Text

<span id="SUMMARYINFO_SIZE"></span><span id="summaryinfo_size"></span>**\_SUMMARYINFO-GRÖßE**  
Im vsglog-Eigenschaftenfenster angezeigter Text – Größe

<span id="SUMMARYINFO_CREATEDBYPIXVERSION"></span><span id="summaryinfo_createdbypixversion"></span>**SUMMARYINFO \_ CREATEDBYPIXVERSION**  
Im vsglog-Eigenschaftenfenster angezeigter Text – erstellt nach Version

<span id="SUMMARYINFO_SESSIONSTARTTIME"></span><span id="summaryinfo_sessionstarttime"></span>**SUMMARYINFO \_ SESSIONSTARTTIME**  
Im vsglog-Eigenschaftenfenster angezeigter Text – Startzeit der Sitzung

<span id="SUMMARYINFO_SYSTEMINFORMATION"></span><span id="summaryinfo_systeminformation"></span>**SUMMARYINFO \_ SYSTEMINFORMATION**  
Text, der im vsglog-Eigenschaftenfenster - Systeminformationen

<span id="SUMMARYINFO_PROCESSOR"></span><span id="summaryinfo_processor"></span>**\_SUMMARYINFO-PROZESSOR**  
Text, der im vsglog-Eigenschaftenfenster – Prozessor angezeigt wird

<span id="SUMMARYINFO_MEMORY"></span><span id="summaryinfo_memory"></span>**\_SUMMARYINFO-ARBEITSSPEICHER**  
Im vsglog-Eigenschaftenfenster – Arbeitsspeicher angezeigter Text

<span id="SUMMARYINFO_OSVERSION"></span><span id="summaryinfo_osversion"></span>**SUMMARYINFO \_ OSVERSION**  
Text, der im vsglog-Eigenschaftenfenster – Betriebssystemversion angezeigt wird

<span id="SUMMARYINFO_OSARCHITECTURE"></span><span id="summaryinfo_osarchitecture"></span>**SUMMARYINFO \_ OSARCHITECTURE**  
Im Vsglog-Eigenschaftenfenster – Betriebssystemarchitektur angezeigter Text

<span id="SUMMARYINFO_TARGETAPPARCHITECTURE"></span><span id="summaryinfo_targetapparchitecture"></span>**SUMMARYINFO \_ TARGETAPPARCHITECTURE**  
Im vsglog-Eigenschaftenfenster – Ziel-App-Architektur angezeigter Text

<span id="SUMMARYINFO_MAXHWFEATURELEVEL"></span><span id="summaryinfo_maxhwfeaturelevel"></span>**SUMMARYINFO \_ MAXHWFEATURELEVEL**  
Text, der im vsglog-Eigenschaftenfenster – Max. Hardwarefeatureebene angezeigt wird

<span id="SUMMARYINFO_DRIVERCONCURRENTCREATES"></span><span id="summaryinfo_driverconcurrentcreates"></span>**SUMMARYINFO \_ DRIVERCONCURRENTCREATES**  
Im vsglog-Beispiel angezeigter Text Eigenschaftenfenster - Driver Concurrent Creates

<span id="SUMMARYINFO_DRIVERCOMMANDLISTS"></span><span id="summaryinfo_drivercommandlists"></span>**SUMMARYINFO \_ DRIVERCOMMANDLISTS**  
In den Vsglog-Befehlslisten Eigenschaftenfenster – Treiberbefehlslisten angezeigter Text

<span id="SUMMARYINFO_DOUBLEPRECISIONSHADERS"></span><span id="summaryinfo_doubleprecisionshaders"></span>**SUMMARYINFO \_ DOUBLEPRECISIONSHADERS**  
Im vsglog-Eigenschaftenfenster – Shader mit doppelter Genauigkeit angezeigter Text

<span id="SUMMARYINFO_DIRECTCOMPUTECS4X"></span><span id="summaryinfo_directcomputecs4x"></span>**SUMMARYINFO \_ DIRECTCOMPUTECS4X**  
Im vsglog-Eigenschaftenfenster – Direct Compute CS 4.x angezeigter Text

<span id="SUMMARYINFO_10BITXRHIGHCOLORFORMAT"></span><span id="summaryinfo_10bitxrhighcolorformat"></span>**SUMMARYINFO \_ 10BITXRHIGHCOLORFORMAT**  
Im vsglog-Format Eigenschaftenfenster 10BITXRHIGHCOLORFORMAT angezeigter Text

<span id="SUMMARYINFO_EXTENDEDCOLORFORMATSUPPORT"></span><span id="summaryinfo_extendedcolorformatsupport"></span>**SUMMARYINFO \_ EXTENDEDCOLORFORMATSUPPORT**  
Text, der im vsglog-Eigenschaftenfenster – Unterstützung für erweitertes Farbformat angezeigt wird

<span id="SUMMARYINFO_DISPLAYINFORMATION"></span><span id="summaryinfo_displayinformation"></span>**SUMMARYINFO \_ DISPLAYINFORMATION**  
Im Vsglog angezeigter Text Eigenschaftenfenster – Anzeigen von Informationen

<span id="SUMMARYINFO_DISPLAYNINFORMATION"></span><span id="summaryinfo_displayninformation"></span>**SUMMARYINFO \_ DISPLAYNINFORMATION**  
Text, der im vsglog-Eigenschaftenfenster – N-Informationen anzeigen angezeigt wird

<span id="SUMMARYINFO_NAME"></span><span id="summaryinfo_name"></span>**\_SUMMARYINFO-NAME**  
Text, der im vsglog-Eigenschaftenfenster – Name angezeigt wird

<span id="SUMMARYINFO_DESCRIPTION"></span><span id="summaryinfo_description"></span>**SUMMARYINFO \_ DESCRIPTION**  
Im Vsglog angezeigter Text Eigenschaftenfenster – Beschreibung

<span id="SUMMARYINFO_DISPLAYMEMORY"></span><span id="summaryinfo_displaymemory"></span>**SUMMARYINFO \_ DISPLAYMEMORY**  
Im Vsglog angezeigter Text Eigenschaftenfenster – Speicher anzeigen

<span id="SUMMARYINFO_DRIVERNAME"></span><span id="summaryinfo_drivername"></span>**SUMMARYINFO \_ DRIVERNAME**  
Im vsglog-Eigenschaftenfenster – Treibername angezeigter Text

<span id="SUMMARYINFO_DRIVERVERSION"></span><span id="summaryinfo_driverversion"></span>**SUMMARYINFO \_ DRIVERVERSION**  
Im vsglog-Eigenschaftenfenster – Treiberversion angezeigter Text

<span id="SUMMARYINFO_MODULEINFORMATION"></span><span id="summaryinfo_moduleinformation"></span>**SUMMARYINFO \_ MODULEINFORMATION**  
Im vsglog-Modul angezeigter Text Eigenschaftenfenster Modulinformationen

<span id="SUMMARYINFO_DIRECT3DINFORMATION"></span><span id="summaryinfo_direct3dinformation"></span>**SUMMARYINFO \_ DIRECT3DINFORMATION**  
Im vsglog-Eigenschaftenfenster – Direct3D-Informationen angezeigter Text

<span id="SUMMARYINFO_VSGVERSION"></span><span id="summaryinfo_vsgversion"></span>**SUMMARYINFO \_ VSGVERSION**  
Im vsglog-Eigenschaftenfenster vsglog- VSG-Version angezeigter Text

<span id="SUMMARYINFO_CAPTUREMACHINE"></span><span id="summaryinfo_capturemachine"></span>**SUMMARYINFO \_ CAPTUREMACHINE**  
Text, der im vsglog-Eigenschaftenfenster – Capture Machine angezeigt wird

<span id="SUMMARYINFO_PLAYBACKMACHINE"></span><span id="summaryinfo_playbackmachine"></span>**SUMMARYINFO \_ PLAYBACKMACHINE**  
Im vsglog-Eigenschaftenfenster – Wiedergabecomputer angezeigter Text

<span id="SUMMARYINFO_REMOTEDATA"></span><span id="summaryinfo_remotedata"></span>**SUMMARYINFO \_ REMOTEDATA**  
Im vsglog-Eigenschaftenfenster – Remotedaten angezeigter Text

<span id="SUMMARYINFO_OtherDirect3DInformation"></span><span id="summaryinfo_otherdirect3dinformation"></span><span id="SUMMARYINFO_OTHERDIRECT3DINFORMATION"></span>**SUMMARYINFO \_ OtherDirect3DInformation**  
Text, der im vsglog-Eigenschaftenfenster – Andere Direct3D-Informationen angezeigt wird

<span id="SUMMARYINFO_SIZEGB"></span><span id="summaryinfo_sizegb"></span>**SUMMARYINFO \_ SIZEGB**  
Text, der im vsglog-Eigenschaftenfenster – Größe GB angezeigt wird

<span id="SUMMARYINFO_SIZEMB"></span><span id="summaryinfo_sizemb"></span>**SUMMARYINFO \_ SIZEMB**  
Text, der im vsglog-Eigenschaftenfenster – Größe MB angezeigt wird

<span id="SUMMARYINFO_SIZEBYTES"></span><span id="summaryinfo_sizebytes"></span>**SUMMARYINFO \_ SIZEBYTES**  
Im Vsglog angezeigter Text Eigenschaftenfenster - Size Bytes

<span id="SUMMARYINFO_MEMORYMB"></span><span id="summaryinfo_memorymb"></span>**SUMMARYINFO \_ MEMORYMB**  
Text, der im vsglog-Eigenschaftenfenster – Arbeitsspeicher MB angezeigt wird

<span id="SUMMARYINFO_X86"></span><span id="summaryinfo_x86"></span>**SUMMARYINFO \_ X86**  
Text, der im vsglog-Eigenschaftenfenster X86 angezeigt wird

<span id="SUMMARYINFO_X64"></span><span id="summaryinfo_x64"></span>**SUMMARYINFO \_ X64**  
Im vsglog-Eigenschaftenfenster X64 angezeigter Text

<span id="SUMMARYINFO_TRUE"></span><span id="summaryinfo_true"></span>**SUMMARYINFO \_ TRUE**  
Text, der im vsglog-Eigenschaftenfenster – True angezeigt wird

<span id="SUMMARYINFO_FALSE"></span><span id="summaryinfo_false"></span>**SUMMARYINFO \_ FALSE**  
Im vsglog-Bereich angezeigter Text Eigenschaftenfenster False

<span id="SUMMARYINFO_ARM32"></span><span id="summaryinfo_arm32"></span>**SUMMARYINFO \_ ARM32**  
Im vsglog-Eigenschaftenfenster – ARM 32 angezeigter Text

<span id="SUMMARYINFO_UNKNOWNCPUARCHITECTURE"></span><span id="summaryinfo_unknowncpuarchitecture"></span>**SUMMARYINFO \_ UNKNOWNCPUARCHITECTURE**  
Text, der im vsglog-Eigenschaftenfenster – Unbekannte CPU-Architektur angezeigt wird

<span id="SUMMARYINFO_AllDXGIFormatValues"></span><span id="summaryinfo_alldxgiformatvalues"></span><span id="SUMMARYINFO_ALLDXGIFORMATVALUES"></span>**SUMMARYINFO \_ AllDXGIFormatValues**  
Im vsglog-Beispiel angezeigter Text Eigenschaftenfenster – Alle DXGI-Formatwerte

<span id="SUMMARYINFO_AllD3D11FormatSupportValues"></span><span id="summaryinfo_alld3d11formatsupportvalues"></span><span id="SUMMARYINFO_ALLD3D11FORMATSUPPORTVALUES"></span>**SUMMARYINFO \_ AllD3D11FormatSupportValues**  
Text, der im vsglog-Eigenschaftenfenster – Alle Unterstützungswerte für das D3D11-Format angezeigt wird

<span id="SUMMARYINFO_D3D11_FEATURE_THREADING"></span><span id="summaryinfo_d3d11_feature_threading"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ THREADING**  
Text, der im vsglog-Eigenschaftenfenster – D3D11 \_ FEATURE \_ THREADING angezeigt wird

<span id="SUMMARYINFO_DriverConcurrentCreates1"></span><span id="summaryinfo_driverconcurrentcreates1"></span><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES1"></span>**\_SUMMARYINFO-TreiberConcurrentCreates1**  
Im vsglog-Beispiel angezeigter Text Eigenschaftenfenster - Driver Concurrent Creates 1

<span id="SUMMARYINFO_DriverCommandLists1"></span><span id="summaryinfo_drivercommandlists1"></span><span id="SUMMARYINFO_DRIVERCOMMANDLISTS1"></span>**\_SUMMARYINFO-TreiberCommandLists1**  
Im vsglog-Abschnitt angezeigter Text Eigenschaftenfenster – Treiberbefehlslisten 1

<span id="SUMMARYINFO_D3D11_FEATURE_DOUBLES"></span><span id="summaryinfo_d3d11_feature_doubles"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ DOUBLES**  
Im vsglog-Eigenschaftenfenster – D3D11 \_ FEATURE \_ DOUBLES angezeigter Text

<span id="SUMMARYINFO_DoublePrecisionFloatShaderOps"></span><span id="summaryinfo_doubleprecisionfloatshaderops"></span><span id="SUMMARYINFO_DOUBLEPRECISIONFLOATSHADEROPS"></span>**SUMMARYINFO \_ DoublePrecisionFloatShaderOps**  
Text, der im vsglog-Eigenschaftenfenster – Float-Shader-Ops mit doppelter Genauigkeit angezeigt wird

<span id="SUMMARYINFO_D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d10_x_hardware_options"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D10 \_ X \_ \_ HARDWAREOPTIONEN**  
Text, der im vsglog-Eigenschaftenfenster – D3D11 \_ FEATURE \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS

<span id="SUMMARYINFO_ComputeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x"></span><span id="summaryinfo_computeshaders_plus_rawandstructuredbuffers_via_shader_4_x"></span><span id="SUMMARYINFO_COMPUTESHADERS_PLUS_RAWANDSTRUCTUREDBUFFERS_VIA_SHADER_4_X"></span>**SUMMARYINFO \_ ComputeShaders \_ Plus \_ RawAndStructuredBuffers \_ Via \_ Shader \_ 4 \_ x**  
Text, der im vsglog-Eigenschaftenfenster – ComputeShaders + Raw und Structure dBuffers über Shader 4.x angezeigt wird

<span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d11_options"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS**  
Text im vsglog-Eigenschaftenfenster – D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS

<span id="SUMMARYINFO_OutputMergerLogicOp"></span><span id="summaryinfo_outputmergerlogicop"></span><span id="SUMMARYINFO_OUTPUTMERGERLOGICOP"></span>**\_SUMMARYINFO-AusgabeMergerLogicOp**  
Text, der im vsglog-Eigenschaftenfenster - Output Merger Logic Op angezeigt wird

<span id="SUMMARYINFO_UAVOnlyRenderingForcedSampleCount"></span><span id="summaryinfo_uavonlyrenderingforcedsamplecount"></span><span id="SUMMARYINFO_UAVONLYRENDERINGFORCEDSAMPLECOUNT"></span>**SUMMARYINFO \_ UAVOnlyRenderingForcedSampleCount**  
Im vsglog-Beispiel angezeigter Text Eigenschaftenfenster – Nur UAV Rendering Forced Sample Count

<span id="SUMMARYINFO_DiscardAPIsSeenByDriver"></span><span id="summaryinfo_discardapisseenbydriver"></span><span id="SUMMARYINFO_DISCARDAPISSEENBYDRIVER"></span>**SUMMARYINFO \_ DiscardAPIsSeenByDriver**  
Text, der im vsglog-Eigenschaftenfenster – ApIs verwerfen angezeigt wird, die vom Treiber angezeigt werden

<span id="SUMMARYINFO_FlagsForUpdateAndCopySeenByDriver"></span><span id="summaryinfo_flagsforupdateandcopyseenbydriver"></span><span id="SUMMARYINFO_FLAGSFORUPDATEANDCOPYSEENBYDRIVER"></span>**\_SUMMARYINFO-FlagsForUpdateAndCopySeenByDriver**  
Text, der im vsglog-Eigenschaftenfenster flags for update and copy Seen By Driver

<span id="SUMMARYINFO_ClearView"></span><span id="summaryinfo_clearview"></span><span id="SUMMARYINFO_CLEARVIEW"></span>**SUMMARYINFO \_ ClearView**  
Text, der im vsglog-Eigenschaftenfenster – Ansicht löschen angezeigt wird

<span id="SUMMARYINFO_CopyWithOverlap"></span><span id="summaryinfo_copywithoverlap"></span><span id="SUMMARYINFO_COPYWITHOVERLAP"></span>**SUMMARYINFO \_ CopyWithOverlap**  
Text, der im vsglog-Eigenschaftenfenster – Kopieren mit Überlappung angezeigt wird

<span id="SUMMARYINFO_ConstantBufferPartialUpdate"></span><span id="summaryinfo_constantbufferpartialupdate"></span><span id="SUMMARYINFO_CONSTANTBUFFERPARTIALUPDATE"></span>**SUMMARYINFO \_ ConstantBufferPartialUpdate**  
Text, der im vsglog-Eigenschaftenfenster : Partielle Aktualisierung des konstanten Puffers angezeigt wird

<span id="SUMMARYINFO_ConstantBufferOffsetting"></span><span id="summaryinfo_constantbufferoffsetting"></span><span id="SUMMARYINFO_CONSTANTBUFFEROFFSETTING"></span>**SUMMARYINFO \_ ConstantBufferOffsetting**  
Text, der im vsglog-Eigenschaftenfenster - Constant Buffer Offsetting angezeigt wird

<span id="SUMMARYINFO_MapNoOverwriteOnDynamicConstantBuffer"></span><span id="summaryinfo_mapnooverwriteondynamicconstantbuffer"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicConstantBuffer**  
Text, der im vsglog-Eigenschaftenfenster - Map No Overwrite On Dynamic Constant Buffer (Keine Überschreibung für dynamischen Konstantenpuffer zuordnen) angezeigt wird

<span id="SUMMARYINFO_MapNoOverwriteOnDynamicBufferSRV"></span><span id="summaryinfo_mapnooverwriteondynamicbuffersrv"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICBUFFERSRV"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicBufferSRV**  
Im vsglog-Abschnitt angezeigter Text Eigenschaftenfenster - Map No Overwrite On Dynamic Buffer SRV

<span id="SUMMARYINFO_MultisampleRTVWithForcedSampleCountOne"></span><span id="summaryinfo_multisamplertvwithforcedsamplecountone"></span><span id="SUMMARYINFO_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE"></span>**SUMMARYINFO \_ MultisampleRTVWithForcedSampleCountOne**  
Im vsglog-Beispiel angezeigter Text Eigenschaftenfenster - Multisample RTV with Forced Sample Count One

<span id="SUMMARYINFO_SAD4ShaderInstructions"></span><span id="summaryinfo_sad4shaderinstructions"></span><span id="SUMMARYINFO_SAD4SHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ SAD4ShaderInstructions**  
Text, der im vsglog-Eigenschaftenfenster – SAD4-Shaderanweisungen angezeigt wird

<span id="SUMMARYINFO_ExtendedDoublesShaderInstructions"></span><span id="summaryinfo_extendeddoublesshaderinstructions"></span><span id="SUMMARYINFO_EXTENDEDDOUBLESSHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ ExtendedDoublesShaderInstructions**  
Text, der in der Vsglog-Eigenschaftenfenster - Extended Doubles Shader Instructions (Anweisungen zum erweiterten Doubles-Shader) angezeigt wird

<span id="SUMMARYINFO_ExtendedResourceSharing"></span><span id="summaryinfo_extendedresourcesharing"></span><span id="SUMMARYINFO_EXTENDEDRESOURCESHARING"></span>**SUMMARYINFO \_ ExtendedResourceSharing**  
Text im vsglog-Eigenschaftenfenster : Erweiterte Ressourcenfreigabe

<span id="SUMMARYINFO_D3D11_FEATURE_ARCHITECTURE_INFO"></span><span id="summaryinfo_d3d11_feature_architecture_info"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ ARCHITECTURE \_ INFO**  
Text, der im vsglog-Eigenschaftenfenster – D3D11 \_ FEATURE \_ ARCHITECTURE \_ INFO

<span id="SUMMARYINFO_TileBasedDeferredRenderer"></span><span id="summaryinfo_tilebaseddeferredrenderer"></span><span id="SUMMARYINFO_TILEBASEDDEFERREDRENDERER"></span>**SUMMARYINFO \_ TileBasedDeferredRenderer**  
Im vsglog-Eigenschaftenfenster – kachelbasierter verzögerter Renderer angezeigter Text

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d9_options"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D9 \_ OPTIONS**  
Text im vsglog-Eigenschaftenfenster – D3D11 \_ FEATURE \_ D3D9 \_ OPTIONS

<span id="SUMMARYINFO_FullNonPow2TextureSupport"></span><span id="summaryinfo_fullnonpow2texturesupport"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORT"></span>**SUMMARYINFO \_ FullNonPow2TextureSupport**  
Text, der im vsglog-Eigenschaftenfenster – vollständige Nicht-Pow2-Texturunterstützung angezeigt wird

<span id="SUMMARYINFO_D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT"></span><span id="summaryinfo_d3d11_feature_shader_min_precision_support"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ SHADER \_ MIN \_ PRECISION \_ SUPPORT**  
Im VSGLOG-Eigenschaftenfenster – D3D11 \_ FEATURE \_ SHADER \_ MIN PRECISION \_ \_ SUPPORT

<span id="SUMMARYINFO_PixelShaderMinPrecision"></span><span id="summaryinfo_pixelshaderminprecision"></span><span id="SUMMARYINFO_PIXELSHADERMINPRECISION"></span>**SUMMARYINFO \_ PixelShaderMinPrecision**  
Im Vsglog angezeigter Text Eigenschaftenfenster – Pixel-Shader– Mindestgenauigkeit

<span id="SUMMARYINFO_AllOtherShaderStagesMinPrecision"></span><span id="summaryinfo_allothershaderstagesminprecision"></span><span id="SUMMARYINFO_ALLOTHERSHADERSTAGESMINPRECISION"></span>**SUMMARYINFO \_ AllOtherShaderStagesMinPrecision**  
Im Vsglog angezeigter Text Eigenschaftenfenster – Alle anderen Shaderstufen– Mindestgenauigkeit

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SHADOW_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_shadow_support"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D9 \_ SHADOW \_ SUPPORT**  
Text im VSGLOG-Eigenschaftenfenster – D3D11 \_ FEATURE \_ D3D9 \_ SHADOW \_ SUPPORT

<span id="SUMMARYINFO_SupportsDepthAsTextureWithLessEqualComparisonFilter"></span><span id="summaryinfo_supportsdepthastexturewithlessequalcomparisonfilter"></span><span id="SUMMARYINFO_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER"></span>**SUMMARYINFO \_ SupportsDepthAsTextureWithLessEqualComparisonFilter**  
Im vsglog-Beispiel angezeigter Text Eigenschaftenfenster – Unterstützt Depth as Texture with Less Equal Comparison Filter (Tiefe als Textur mit einem weniger gleichgestellten Vergleichsfilter)

<span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d11_options1"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS1**  
Im vsglog-Eigenschaftenfenster – D3D11 \_ FEATURE \_ D3D11 OPTIONS1 angezeigter \_ Text

<span id="SUMMARYINFO_TiledResourcesTier"></span><span id="summaryinfo_tiledresourcestier"></span><span id="SUMMARYINFO_TILEDRESOURCESTIER"></span>**SUMMARYINFO \_ TiledResourcesTier**  
Text, der im vsglog-Eigenschaftenfenster – Ebene "Gekachelte Ressourcen" angezeigt wird

<span id="SUMMARYINFO_MinMaxFiltering"></span><span id="summaryinfo_minmaxfiltering"></span><span id="SUMMARYINFO_MINMAXFILTERING"></span>**SUMMARYINFO \_ MinMaxFiltering**  
Text, der im vsglog-Eigenschaftenfenster – Min Max Filtering (Max. Filterung) angezeigt wird

<span id="SUMMARYINFO_ClearViewAlsoSupportsDepthOnlyFormats"></span><span id="summaryinfo_clearviewalsosupportsdepthonlyformats"></span><span id="SUMMARYINFO_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS"></span>**SUMMARYINFO \_ ClearViewAlsoSupportsDepthOnlyFormats**  
Text, der im vsglog-Eigenschaftenfenster - Clear View angezeigt wird, unterstützt auch nur Tiefenformate.

<span id="SUMMARYINFO_MapOnDefaultBuffers"></span><span id="summaryinfo_mapondefaultbuffers"></span><span id="SUMMARYINFO_MAPONDEFAULTBUFFERS"></span>**SUMMARYINFO \_ MapOnDefaultBuffers**  
Text, der im vsglog-Eigenschaftenfenster – Zuordnung zu Standardpuffern angezeigt wird

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_simple_instancing_support"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D9 \_ SIMPLE \_ INSTANCING \_ SUPPORT**  
Text im VSGLOG-Eigenschaftenfenster – D3D11 \_ FEATURE \_ D3D9 \_ SIMPLE \_ INSTANCING \_ SUPPORT

<span id="SUMMARYINFO_SimpleInstancingSupported0"></span><span id="summaryinfo_simpleinstancingsupported0"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED0"></span>**SUMMARYINFO \_ SimpleInstancingSupported0**  
Text, der im vsglog-Eigenschaftenfenster – Simple Instancing Supported 0 (Einfache Instancing unterstützt 0) angezeigt wird

<span id="SUMMARYINFO_D3D11_FEATURE_MARKER_SUPPORT"></span><span id="summaryinfo_d3d11_feature_marker_support"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE MARKER SUPPORT (FEATUREMARKERUNTERSTÜTZUNG FÜR SUMMARYINFO D3D11) \_ \_**  
Text, der im VSGLOG-Eigenschaftenfenster – D3D11 \_ FEATURE \_ MARKER \_ SUPPORT

<span id="SUMMARYINFO_Profile"></span><span id="summaryinfo_profile"></span><span id="SUMMARYINFO_PROFILE"></span>**\_SUMMARYINFO-Profil**  
Im vsglog-Profil Eigenschaftenfenster angezeigter Text

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d9_options1"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D9 \_ OPTIONS1**  
Text im vsglog-Eigenschaftenfenster – D3D11 \_ FEATURE \_ D3D9 \_ OPTIONS1

<span id="SUMMARYINFO_FullNonPow2TextureSupported"></span><span id="summaryinfo_fullnonpow2texturesupported"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORTED"></span>**SUMMARYINFO \_ FullNonPow2TextureSupported**  
Text, der im vsglog-Eigenschaftenfenster - Full Non-Pow2 Texture Supported (Vollständige Nicht-Pow2-Textur unterstützt) angezeigt wird

<span id="SUMMARYINFO_DepthAsTextureWithLessEqualComparisonFilterSupported"></span><span id="summaryinfo_depthastexturewithlessequalcomparisonfiltersupported"></span><span id="SUMMARYINFO_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED"></span>**SUMMARYINFO \_ DepthAsTextureWithLessEqualComparisonFilterSupported**  
Im vsglog-Beispiel angezeigter Text Eigenschaftenfenster - Depth As Texture with Less Equal Comparison Filter Supported

<span id="SUMMARYINFO_SimpleInstancingSupported1"></span><span id="summaryinfo_simpleinstancingsupported1"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED1"></span>**SUMMARYINFO \_ SimpleInstancingSupported1**  
Im vsglog-Beispiel angezeigter Text Eigenschaftenfenster – Simple Instancing Supported 1

<span id="SUMMARYINFO_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported"></span><span id="summaryinfo_texturecubefacerendertargetwithnoncubedepthstencilsupported"></span><span id="SUMMARYINFO_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED"></span>**SUMMARYINFO \_ TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported**  
Text, der im vsglog-Eigenschaftenfenster - Texture Cube Face Render Target with Non-Cube Depth Stencil Supported

<span id="SUMMARYINFO_DXGIFormat"></span><span id="summaryinfo_dxgiformat"></span><span id="SUMMARYINFO_DXGIFORMAT"></span>**SUMMARYINFO \_ DXGIFormat**  
Text, der im vsglog-Eigenschaftenfenster – DXGIFormat angezeigt wird

<span id="SUMMARYINFO_DXGIFormat1"></span><span id="summaryinfo_dxgiformat1"></span><span id="SUMMARYINFO_DXGIFORMAT1"></span>**SUMMARYINFO \_ DXGIFormat1**  
Im vsglog-Beispiel angezeigter Text Eigenschaftenfenster DXGIFormat1

<span id="SUMMARYINFO_MODULENAME"></span><span id="summaryinfo_modulename"></span>**SUMMARYINFO \_ MODULENAME**  
Text, der im vsglog-Eigenschaftenfenster - MODULENAME angezeigt wird

<span id="IDD_CONFIGURATION"></span><span id="idd_configuration"></span>**\_IDD-KONFIGURATION**  
Im Dialogfeld "Firewall konfigurieren" in VsGraphicsRemoteEngine angezeigter Text

<span id="IDC_STATIC_HEADER_ICON"></span><span id="idc_static_header_icon"></span>**SYMBOL FÜR STATISCHE \_ \_ IDC-HEADER \_**  
Im Dialogfeld "Firewall konfigurieren" angezeigter Text – Statisches Headersymbol

<span id="IDC_STATIC_HEADER"></span><span id="idc_static_header"></span>**STATISCHER \_ \_ IDC-HEADER**  
Im Dialogfeld "Firewall konfigurieren" angezeigter Text – Statischer Header

<span id="IDC_STATIC_FW_CONFIGURATION"></span><span id="idc_static_fw_configuration"></span>**STATISCHE \_ \_ IDC-FW-KONFIGURATION \_**  
Im Dialogfeld "Firewall konfigurieren" angezeigter Text – Statische Firewallkonfiguration

<span id="IDC_STATIC_FW_ICON"></span><span id="idc_static_fw_icon"></span>**SYMBOL FÜR \_ \_ STATISCHES IDC-FW \_**  
Im Dialogfeld "Firewall konfigurieren" angezeigter Text – Symbol "Statische Firewall"

<span id="IDC_STATIC_FW_HEADER"></span><span id="idc_static_fw_header"></span>**STATISCHER \_ \_ IDC-FW-HEADER \_**  
Im Dialogfeld "Firewall konfigurieren" angezeigter Text – Statischer Firewallheader

<span id="IDC_STATIC_GROUPBOX_FW"></span><span id="idc_static_groupbox_fw"></span>**IDC \_ STATIC \_ GROUPBOX \_ FW**  
Im Dialogfeld "Firewall konfigurieren" angezeigter Text – Statische Groupbox-Firewall

<span id="IDC_CHECK_FW_DOMAIN_NETWORKS"></span><span id="idc_check_fw_domain_networks"></span>**IDC \_ CHECK \_ FW \_ DOMAIN \_ NETWORKS**  
Im Dialogfeld "Firewall konfigurieren" angezeigter Text – Überprüfen von Firewalldomänennetzwerken

<span id="IDC_CHECK_FW_PRIVATE_NETWORKS"></span><span id="idc_check_fw_private_networks"></span>**IDC \_ CHECK \_ FW \_ PRIVATE \_ NETWORKS**  
Im Dialogfeld "Firewall konfigurieren" angezeigter Text – Überprüfen privater Firewallnetzwerke

<span id="IDC_CHECK_FW_PUBLIC_NETWORKS"></span><span id="idc_check_fw_public_networks"></span>**IDC \_ CHECK \_ FW \_ PUBLIC \_ NETWORKS**  
Im Dialogfeld "Firewall konfigurieren" angezeigter Text – Überprüfen der öffentlichen Firewallnetzwerke

<span id="IDC_BUTTON_CONFIGURE"></span><span id="idc_button_configure"></span>**\_IDC-SCHALTFLÄCHE \_ KONFIGURIEREN**  
Im Dialogfeld "Firewall konfigurieren" angezeigter Text – Schaltfläche "Konfigurieren"

<span id="ID_CONFIGURATION_CANCEL"></span><span id="id_configuration_cancel"></span>**ID \_ CONFIGURATION \_ CANCEL**  
Im Dialogfeld "Firewall konfigurieren" angezeigter Text – Konfigurations abbrechen

<span id="IDS_TEXT_FW_NOT_CONFIGURED"></span><span id="ids_text_fw_not_configured"></span>**IDS \_ TEXT \_ FW \_ NOT \_ CONFIGURED**  
Text im Dialogfeld "Firewall konfigurieren" – Textfirewall nicht konfiguriert

<span id="IDS_TEXT_FW_CONFIGURED"></span><span id="ids_text_fw_configured"></span>**IDS \_ TEXT \_ FW \_ CONFIGURED**  
Im Dialogfeld Firewall konfigurieren angezeigter Text – Textfirewall konfiguriert

<span id="IDS_FIREWALL_RULE_NAME"></span><span id="ids_firewall_rule_name"></span>**NAME DER \_ IDS-FIREWALLREGEL \_ \_**  
Im Dialogfeld Firewall konfigurieren angezeigter Text – Firewallregelname

<span id="IDS_FIREWALL_RULE_DESCRIPTION"></span><span id="ids_firewall_rule_description"></span>**BESCHREIBUNG DER \_ IDS-FIREWALLREGEL \_ \_**  
Im Dialogfeld Firewall konfigurieren angezeigter Text – Firewallregelbeschreibung

<span id="IDS_STATIC_HEADER"></span><span id="ids_static_header"></span>**STATISCHER \_ \_ IDS-HEADER**  
Im Dialogfeld Firewall konfigurieren – Statischer Header angezeigter Text

<span id="IDS_CONFIGURATION_TITLE"></span><span id="ids_configuration_title"></span>**\_IDS-KONFIGURATIONSTITEL \_**  
Im Dialogfeld Firewall konfigurieren angezeigter Text – Konfigurationstitel

<span id="IDS_STATIC_FW_HEADER"></span><span id="ids_static_fw_header"></span>**STATISCHER \_ \_ IDS-FW-HEADER \_**  
Im Dialogfeld Firewall konfigurieren angezeigter Text – Statischer Firewallheader

<span id="IDS_STATIC_GROUPBOX_FW"></span><span id="ids_static_groupbox_fw"></span>**IDS \_ STATIC \_ GROUPBOX \_ FW**  
Text, der im Dialogfeld Firewall konfigurieren – Statische Gruppenfeldfirewall angezeigt wird

<span id="IDS_CHECK_FW_DOMAIN_NETWORKS"></span><span id="ids_check_fw_domain_networks"></span>**IDS \_ CHECK \_ FW \_ DOMAIN \_ NETWORKS**  
Im Dialogfeld Firewall konfigurieren angezeigter Text – Überprüfen von Firewalldomänennetzwerken

<span id="IDS_CHECK_FW_PRIVATE_NETWORKS"></span><span id="ids_check_fw_private_networks"></span>**IDS \_ CHECK \_ FW \_ PRIVATE \_ NETWORKS**  
Im Dialogfeld Firewall konfigurieren angezeigter Text: Überprüfen privater Firewallnetzwerke

<span id="IDS_CHECK_FW_PUBLIC_NETWORKS"></span><span id="ids_check_fw_public_networks"></span>**IDS \_ CHECK \_ FW \_ PUBLIC \_ NETWORKS**  
Text, der im Dialogfeld Firewall konfigurieren angezeigt wird: Überprüfen von öffentlichen Firewallnetzwerken

<span id="IDS_BUTTON_CONFIGURE"></span><span id="ids_button_configure"></span>**SCHALTFLÄCHE \_ "IDS" \_ KONFIGURIEREN**  
Im Dialogfeld Firewall konfigurieren angezeigter Text – Buttom Confiture

<span id="IDS_CONFIGURATION_CANCEL"></span><span id="ids_configuration_cancel"></span>**IDS \_ CONFIGURATION \_ CANCEL**  
Im Dialogfeld "Firewall konfigurieren" angezeigter Text : Konfigurations abbrechen

<span id="IDS_CAPTURETOOLTIP_MESSAGE_CORESYSTEM"></span><span id="ids_capturetooltip_message_coresystem"></span>**IDS \_ CAPTURETOOLTIP \_ MESSAGE \_ CORESYSTEM**  
Ressourcen-ID für zeichenfolge "Use the capture button in Visual Studio to capture frame(s)." (Verwenden Sie die Erfassungsschaltfläche in Visual Studio, um Frames zu erfassen.)

<span id="IDS_ET_NONE"></span><span id="ids_et_none"></span>**IDS \_ ET \_ NONE**  
Wird nicht verwendet.

<span id="IDS_ET_SESSIONSTART"></span><span id="ids_et_sessionstart"></span>**IDS \_ ET \_ SESSIONSTART**  
Wird nicht verwendet.

<span id="IDS_ET_SESSIONEND"></span><span id="ids_et_sessionend"></span>**IDS \_ ET \_ SESSIONEND**  
Wird nicht verwendet.

<span id="IDS_ET_PROCESSSTART"></span><span id="ids_et_processstart"></span>**IDS \_ ET \_ PROCESSSTART**  
Wird nicht verwendet.

<span id="IDS_ET_PROCESSEND"></span><span id="ids_et_processend"></span>**IDS \_ ET \_ PROCESSEND**  
Wird nicht verwendet.

<span id="IDS_ET_FRAMEBEGIN"></span><span id="ids_et_framebegin"></span>**IDS \_ ET \_ FRAMEBEGIN**  
Wird nicht verwendet.

<span id="IDS_ET_FRAMEEND"></span><span id="ids_et_frameend"></span>**IDS \_ ET \_ FRAMEEND**  
Wird nicht verwendet.

<span id="IDS_ET_USEREVENTBEGIN"></span><span id="ids_et_usereventbegin"></span>**IDS \_ ET \_ USEREVENTBEGIN**  
Wird nicht verwendet.

<span id="IDS_ET_USEREVENTEND"></span><span id="ids_et_usereventend"></span>**IDS \_ ET \_ USEREVENTEND**  
Wird nicht verwendet.

<span id="IDS_ET_USERMARKER"></span><span id="ids_et_usermarker"></span>**IDS \_ ET \_ USERMARKER**  
Wird nicht verwendet.

<span id="IDS_ET_CALL"></span><span id="ids_et_call"></span>**IDS \_ ET \_ CALL**  
Wird nicht verwendet.

<span id="IDS_ET_OBJECTPOPULATION"></span><span id="ids_et_objectpopulation"></span>**IDS \_ ET \_ OBJECTPOPULATION**  
Wird nicht verwendet.

<span id="IDS_ET_OBJECTCREATION"></span><span id="ids_et_objectcreation"></span>**IDS \_ ET \_ OBJECTCREATION**  
Wird nicht verwendet.

<span id="IDS_ET_CALLSYNC"></span><span id="ids_et_callsync"></span>**IDS \_ ET \_ CALLSYNC**  
Wird nicht verwendet.

<span id="IDS_ET_UNKNOWN"></span><span id="ids_et_unknown"></span>**IDS \_ ET \_ UNKNOWN**  
Wird nicht verwendet.

<span id="IDS_TRIGGER_NONE"></span><span id="ids_trigger_none"></span>**IDS \_ TRIGGER \_ NONE**  
Wird nicht verwendet.

<span id="IDS_TRIGGER_PROGRAMSTART"></span><span id="ids_trigger_programstart"></span>**IDS \_ TRIGGER \_ PROGRAMSTART**  
Wird nicht verwendet.

<span id="IDS_TRIGGER_FRAME"></span><span id="ids_trigger_frame"></span>**IDS \_ TRIGGER \_ FRAME**  
Wird nicht verwendet.

<span id="IDS_TRIGGER_TIME"></span><span id="ids_trigger_time"></span>**IDS \_ TRIGGER \_ TIME**  
Wird nicht verwendet.

<span id="IDS_TRIGGER_USERMARKER"></span><span id="ids_trigger_usermarker"></span>**IDS \_ TRIGGER \_ USERMARKER**  
Wird nicht verwendet.

<span id="IDS_TRIGGER_BEGINUSEREVENT"></span><span id="ids_trigger_beginuserevent"></span>**IDS \_ TRIGGER \_ BEGINUSEREVENT**  
Wird nicht verwendet.

<span id="IDS_TRIGGER_ENDUSEREVENT"></span><span id="ids_trigger_enduserevent"></span>**IDS \_ TRIGGER \_ ENDUSEREVENT**  
Wird nicht verwendet.

<span id="IDS_TRIGGER_CAPTUREFRAME"></span><span id="ids_trigger_captureframe"></span>**IDS \_ TRIGGER \_ CAPTUREFRAME**  
Wird nicht verwendet.

<span id="IDS_TRIGGER_APICAPTURE"></span><span id="ids_trigger_apicapture"></span>**IDS \_ TRIGGER \_ APICAPTURE**  
Wird nicht verwendet.

<span id="IDS_ERROR_CALLDATA"></span><span id="ids_error_calldata"></span>**\_IDS-FEHLER \_ CALLDATA**  
Wird nicht verwendet.

<span id="IDS_ERROR_CREATINGLOG"></span><span id="ids_error_creatinglog"></span>**IDS \_ ERROR \_ CREATINGLOG**  
Wird nicht verwendet.

<span id="IDS_UNKNOWNCALL"></span><span id="ids_unknowncall"></span>**IDS \_ UNKNOWNCALL**  
Wird nicht verwendet.

<span id="IDS_WARN_FEATURE_LEVEL_CHANGED"></span><span id="ids_warn_feature_level_changed"></span>**IDS \_ WARN \_ FEATURE \_ LEVEL \_ CHANGED**  
Wird nicht verwendet.

<span id="ID_STATUS_FREQUENCY"></span><span id="id_status_frequency"></span>**HÄUFIGKEIT \_ DES ID-STATUS \_**  

<span id="ID_DISABLE_HUD"></span><span id="id_disable_hud"></span>**ID \_ DISABLE \_ HUD**  

<span id="ID_DISABLE_COMPAT"></span><span id="id_disable_compat"></span>**ID \_ DISABLE \_ COMPAT**  

<span id="ID_COLLECT_CALLSTACKS"></span><span id="id_collect_callstacks"></span>**ID \_ COLLECT \_ CALLSTACKS**  

<span id="ID_ENABLE_SDKERROR_STOP"></span><span id="id_enable_sdkerror_stop"></span>**ID \_ ENABLE \_ SDKERROR \_ STOP**  

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



