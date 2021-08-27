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
ms.openlocfilehash: 5012a6dc40f47a396139eb29f2f88151b4a10ffb
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623156"
---
# <a name="span-idvspixengineresource_idspanresource_id-enumeration"></a><span id="vspixengine.resource_id"></span>\_Ressourcen-ID-Enumeration

Definiert Ressourcen-IDs für freigegebene Zeichenfolgenressourcen. Diese werden vom Host an die Erfassungs-Engine übergeben. Sie werden verwendet, um Zeichenfolgen in der HUD-Überlagerung der erfassten App anzuzeigen oder Registrierungswerte von Visual Studio Optionen an die Erfassungs-ENGI zu übergeben.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="IDS_ENGINEDISCONNECTED"></span><span id="ids_enginedisconnected"></span>**\_IDS-ENGINEDISCONNECTED**  
Nicht verwendet. Ressourcen-ID für zeichenfolge, die zuvor verwendet wurde, um anzugeben, dass der Druckbildschirm nach Abschluss der Aufzeichnungssitzung erreicht wurde.

<span id="IDR_RCDATA1"></span><span id="idr_rcdata1"></span>**IDR \_ RCDATA1**  
Nicht verwendet.

<span id="IDS_DEFAULTEXPFILE_CONTENT"></span><span id="ids_defaultexpfile_content"></span>**IDS \_ \_ DEFAULTEXPFILE-INHALT**  
Nicht verwendet. Ressourcen-ID für Zeichenfolge, die zuvor in Legacyerfassungsszenarien für XML-Daten verwendet wurde.

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
Ressourcen-ID für die Zeichenfolge "DCOMP wird von der App verwendet, wird aber unter diesem Betriebssystem nicht unterstützt"

<span id="IDS_DWRITE_NOT_SUPPORTED"></span><span id="ids_dwrite_not_supported"></span>**IDS \_ DWRITE \_ WIRD NICHT \_ UNTERSTÜTZT**  
Ressourcen-ID für die Zeichenfolge "DWRITE wird von der App verwendet, wird aber unter diesem Betriebssystem nicht unterstützt"

<span id="IDS_EXPECTED_FAILURE_FORMAT"></span><span id="ids_expected_failure_format"></span>**IDS \_ EXPECTED \_ FAILURE \_ FORMAT**  
Die Ressourcen-ID für die Zeichenfolge "%s hat während der Wiedergabe einen Fehler zurückgegeben. (HRESULT=%s) \\ r \\ n".

<span id="IDS_CAPTURETOOLTIP_MESSAGE"></span><span id="ids_capturetooltip_message"></span>**IDS \_ CAPTURETOOLTIP \_ MESSAGE**  
Ressourcen-ID für die Zeichenfolge "Verwenden Sie die Taste "Druckbildschirm", um einen Frame zu erfassen."

<span id="IDS_D2D_AND_D10_NOT_SUPPORTED"></span><span id="ids_d2d_and_d10_not_supported"></span>**IDS \_ D2D \_ UND \_ D10 \_ WERDEN NICHT \_ UNTERSTÜTZT**  
Ressourcen-ID für die Zeichenfolge "D2D und D10 werden auf diesem Betriebssystem nicht gemeinsam unterstützt"

<span id="IDS_HUD_STATISTICS"></span><span id="ids_hud_statistics"></span>**IDS \_ HUD \_ STATISTICS**  
Ressourcen-ID für zeichenfolge "Frames captured %d. Framezeit (ms) %0,00f"

<span id="IDS_INTERNAL_METHOD"></span><span id="ids_internal_method"></span>**INTERNE \_ \_ IDS-METHODE**  
Ressourcen-ID für die Zeichenfolge "Directx Internal Method"

<span id="IDS_CAPTURE_FRAME_MARK"></span><span id="ids_capture_frame_mark"></span>**IDS \_ CAPTURE \_ FRAME \_ MARK**  
Ressourcen-ID für die Zeichenfolge "Captured Frame %ld"

<span id="PIPELINESTAGE_INPUTASSEMBLER"></span><span id="pipelinestage_inputassembler"></span>**PIPELINESTAGE \_ INPUTASSEMBLER**  
Nicht verwendet.

<span id="PIPELINESTAGE_VERTEXSHADER"></span><span id="pipelinestage_vertexshader"></span>**PIPELINESTAGE \_ VERTEXSHADER**  
Nicht verwendet.

<span id="PIPELINESTAGE_HULLSHADER"></span><span id="pipelinestage_hullshader"></span>**PIPELINESTAGE \_ HULLSHADER**  
Nicht verwendet.

<span id="PIPELINESTAGE_TESSELATOR"></span><span id="pipelinestage_tesselator"></span>**\_PIPELINESTAGE-TESSELATOR**  
Nicht verwendet.

<span id="PIPELINESTAGE_DOMAINSHADER"></span><span id="pipelinestage_domainshader"></span>**PIPELINESTAGE \_ DOMAINSHADER**  
Nicht verwendet.

<span id="PIPELINESTAGE_GEOMETRYSHADER"></span><span id="pipelinestage_geometryshader"></span>**PIPELINESTAGE \_ GEOMETRYSHADER**  
Nicht verwendet.

<span id="PIPELINESTAGE_STREAMOUTPUT"></span><span id="pipelinestage_streamoutput"></span>**PIPELINESTAGE \_ STREAMOUTPUT**  
Nicht verwendet.

<span id="PIPELINESTAGE_RASTERIZER"></span><span id="pipelinestage_rasterizer"></span>**\_PIPELINESTAGE-RASTERIZER**  
Nicht verwendet.

<span id="PIPELINESTAGE_PIXELSHADER"></span><span id="pipelinestage_pixelshader"></span>**PIPELINESTAGE \_ PIXELSHADER**  
Nicht verwendet.

<span id="PIPELINESTAGE_OUTPUTMERGER"></span><span id="pipelinestage_outputmerger"></span>**PIPELINESTAGE \_ OUTPUTMERGER**  
Nicht verwendet.

<span id="PIPELINESTAGE_COMPUTESHADER"></span><span id="pipelinestage_computeshader"></span>**PIPELINESTAGE \_ COMPUTESHADER**  
Nicht verwendet.

<span id="BUFFEROBJECT_SUPPORTEDFORMAT"></span><span id="bufferobject_supportedformat"></span>**BUFFEROBJECT \_ SUPPORTEDFORMAT**  
Nicht verwendet.

<span id="BUFFEROBJECT_CURRENTFORMAT"></span><span id="bufferobject_currentformat"></span>**BUFFEROBJECT \_ CURRENTFORMAT**  
Nicht verwendet.

<span id="BUFFEROBJECT_HEADER"></span><span id="bufferobject_header"></span>**\_BUFFEROBJECT-HEADER**  
Nicht verwendet.

<span id="BUFFEROBJECT_LINE"></span><span id="bufferobject_line"></span>**BUFFEROBJECT \_ LINE**  
Nicht verwendet.

<span id="BUFFEROBJECT_INVALIDFORMAT"></span><span id="bufferobject_invalidformat"></span>**BUFFEROBJECT \_ INVALIDFORMAT**  
Nicht verwendet.

<span id="BUFFEROBJECT_INVALIDEMPTYFORMAT"></span><span id="bufferobject_invalidemptyformat"></span>**BUFFEROBJECT \_ INVALIDEMPTYFORMAT**  
Nicht verwendet.

<span id="BUFFEROBJECT_INVALIDFORMATSIZE"></span><span id="bufferobject_invalidformatsize"></span>**BUFFEROBJECT \_ INVALIDFORMATSIZE**  
Nicht verwendet.

<span id="SUMMARYINFO_TARGETAPPLICATION"></span><span id="summaryinfo_targetapplication"></span>**SUMMARYINFO \_ TARGETAPPLICATION**  
Im Vsglog-Eigenschaftenfenster angezeigter Text – Zielanwendung

<span id="SUMMARYINFO_PATH"></span><span id="summaryinfo_path"></span>**\_SUMMARYINFO-PFAD**  
Im vsglog-Eigenschaftenfenster angezeigter Text – Pfad

<span id="SUMMARYINFO_TARGETVERSION"></span><span id="summaryinfo_targetversion"></span>**SUMMARYINFO \_ TARGETVERSION**  
Im vsglog-Eigenschaftenfenster – Zielversion angezeigter Text

<span id="SUMMARYINFO_LASTMODIFIEDDATE"></span><span id="summaryinfo_lastmodifieddate"></span>**SUMMARYINFO \_ LASTMODIFIEDDATE**  
Im vsglog-Eigenschaftenfenster angezeigter Text – Datum der letzten Änderung

<span id="SUMMARYINFO_PROCESSID"></span><span id="summaryinfo_processid"></span>**SUMMARYINFO \_ PROCESSID**  
Im vsglog-Eigenschaftenfenster angezeigter Text – Prozess-ID

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
Im vsglog-Eigenschaftenfenster – Prozessor angezeigter Text

<span id="SUMMARYINFO_MEMORY"></span><span id="summaryinfo_memory"></span>**\_SUMMARYINFO-ARBEITSSPEICHER**  
Text, der im vsglog-Eigenschaftenfenster – Arbeitsspeicher angezeigt wird

<span id="SUMMARYINFO_OSVERSION"></span><span id="summaryinfo_osversion"></span>**SUMMARYINFO \_ OSVERSION**  
Text, der im vsglog-Eigenschaftenfenster – Betriebssystemversion angezeigt wird

<span id="SUMMARYINFO_OSARCHITECTURE"></span><span id="summaryinfo_osarchitecture"></span>**SUMMARYINFO \_ OSARCHITECTURE**  
Im Vsglog-Eigenschaftenfenster – Betriebssystemarchitektur angezeigter Text

<span id="SUMMARYINFO_TARGETAPPARCHITECTURE"></span><span id="summaryinfo_targetapparchitecture"></span>**SUMMARYINFO \_ TARGETAPPARCHITECTURE**  
Text, der im vsglog-Eigenschaftenfenster – Architektur der Ziel-App angezeigt wird

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
Im vsglog-Eigenschaftenfenster – N-Informationen anzeigen angezeigter Text

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
Text, der im vsglog-Eigenschaftenfenster VSG-Version angezeigt wird

<span id="SUMMARYINFO_CAPTUREMACHINE"></span><span id="summaryinfo_capturemachine"></span>**SUMMARYINFO \_ CAPTUREMACHINE**  
Text, der im vsglog-Eigenschaftenfenster – Capture Machine angezeigt wird

<span id="SUMMARYINFO_PLAYBACKMACHINE"></span><span id="summaryinfo_playbackmachine"></span>**SUMMARYINFO \_ PLAYBACKMACHINE**  
Im vsglog-Eigenschaftenfenster – Wiedergabecomputer angezeigter Text

<span id="SUMMARYINFO_REMOTEDATA"></span><span id="summaryinfo_remotedata"></span>**SUMMARYINFO \_ REMOTEDATA**  
Im vsglog-Eigenschaftenfenster – Remotedaten angezeigter Text

<span id="SUMMARYINFO_OtherDirect3DInformation"></span><span id="summaryinfo_otherdirect3dinformation"></span><span id="SUMMARYINFO_OTHERDIRECT3DINFORMATION"></span>**SUMMARYINFO \_ OtherDirect3DInformation**  
Text, der im vsglog-Eigenschaftenfenster – Andere Direct3D-Informationen angezeigt wird

<span id="SUMMARYINFO_SIZEGB"></span><span id="summaryinfo_sizegb"></span>**SUMMARYINFO \_ SIZEGB**  
Im Vsglog angezeigter Text Eigenschaftenfenster – Größe GB

<span id="SUMMARYINFO_SIZEMB"></span><span id="summaryinfo_sizemb"></span>**SUMMARYINFO \_ SIZEMB**  
Text, der im vsglog-Eigenschaftenfenster – Größe MB angezeigt wird

<span id="SUMMARYINFO_SIZEBYTES"></span><span id="summaryinfo_sizebytes"></span>**SUMMARYINFO \_ SIZEBYTES**  
Im Vsglog angezeigter Text Eigenschaftenfenster – Größe Bytes

<span id="SUMMARYINFO_MEMORYMB"></span><span id="summaryinfo_memorymb"></span>**SUMMARYINFO \_ MEMORYMB**  
Im vsglog-Bereich angezeigter Text Eigenschaftenfenster – Arbeitsspeicher MB

<span id="SUMMARYINFO_X86"></span><span id="summaryinfo_x86"></span>**SUMMARYINFO \_ X86**  
Im vsglog-Eigenschaftenfenster X86 angezeigter Text

<span id="SUMMARYINFO_X64"></span><span id="summaryinfo_x64"></span>**SUMMARYINFO \_ X64**  
Im vsglog-Eigenschaftenfenster X64 angezeigter Text

<span id="SUMMARYINFO_TRUE"></span><span id="summaryinfo_true"></span>**SUMMARYINFO \_ TRUE**  
Im vsglog-Eigenschaftenfenster angezeigter Text : True

<span id="SUMMARYINFO_FALSE"></span><span id="summaryinfo_false"></span>**SUMMARYINFO \_ FALSE**  
Im vsglog-Bereich angezeigter Text Eigenschaftenfenster False

<span id="SUMMARYINFO_ARM32"></span><span id="summaryinfo_arm32"></span>**SUMMARYINFO \_ ARM32**  
Im vsglog-Eigenschaftenfenster – ARM 32 angezeigter Text

<span id="SUMMARYINFO_UNKNOWNCPUARCHITECTURE"></span><span id="summaryinfo_unknowncpuarchitecture"></span>**SUMMARYINFO \_ UNKNOWNCPUARCHITECTURE**  
Im vsglog-Eigenschaftenfenster – Unbekannte CPU-Architektur angezeigter Text

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
Text, der im vsglog-Eigenschaftenfenster – Gleitkomma-Shader-Ops mit doppelter Genauigkeit angezeigt wird

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
Text, der im vsglog-Eigenschaftenfenster – Vom Treiber angezeigte APIs verwerfen angezeigt wird

<span id="SUMMARYINFO_FlagsForUpdateAndCopySeenByDriver"></span><span id="summaryinfo_flagsforupdateandcopyseenbydriver"></span><span id="SUMMARYINFO_FLAGSFORUPDATEANDCOPYSEENBYDRIVER"></span>**\_SUMMARYINFO-FlagsForUpdateAndCopySeenByDriver**  
Im vsglog-Beispiel angezeigter Text Eigenschaftenfenster flags for update and copy Seen By Driver (Flags für Update und Kopie, die vom Treiber angezeigt werden)

<span id="SUMMARYINFO_ClearView"></span><span id="summaryinfo_clearview"></span><span id="SUMMARYINFO_CLEARVIEW"></span>**SUMMARYINFO \_ ClearView**  
Im Vsglog angezeigter Text Eigenschaftenfenster - Clear View

<span id="SUMMARYINFO_CopyWithOverlap"></span><span id="summaryinfo_copywithoverlap"></span><span id="SUMMARYINFO_COPYWITHOVERLAP"></span>**SUMMARYINFO \_ CopyWithOverlap**  
Text, der im vsglog-Eigenschaftenfenster – Kopieren mit Überlappung angezeigt wird

<span id="SUMMARYINFO_ConstantBufferPartialUpdate"></span><span id="summaryinfo_constantbufferpartialupdate"></span><span id="SUMMARYINFO_CONSTANTBUFFERPARTIALUPDATE"></span>**SUMMARYINFO \_ ConstantBufferPartialUpdate**  
Text, der im vsglog-Eigenschaftenfenster - Constant Buffer Partial Update (Teilaktualisierung des konstanten Puffers) angezeigt wird

<span id="SUMMARYINFO_ConstantBufferOffsetting"></span><span id="summaryinfo_constantbufferoffsetting"></span><span id="SUMMARYINFO_CONSTANTBUFFEROFFSETTING"></span>**SUMMARYINFO \_ ConstantBufferOffsetting**  
Text, der im vsglog-Eigenschaftenfenster - Constant Buffer Offsetting angezeigt wird

<span id="SUMMARYINFO_MapNoOverwriteOnDynamicConstantBuffer"></span><span id="summaryinfo_mapnooverwriteondynamicconstantbuffer"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicConstantBuffer**  
Text, der im vsglog-Eigenschaftenfenster - Map No Overwrite On Dynamic Constant Buffer (Keine Überschreibung für dynamischen Konstantenpuffer zuordnen) angezeigt wird

<span id="SUMMARYINFO_MapNoOverwriteOnDynamicBufferSRV"></span><span id="summaryinfo_mapnooverwriteondynamicbuffersrv"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICBUFFERSRV"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicBufferSRV**  
Text, der im vsglog-Eigenschaftenfenster – Zuordnung kein Überschreiben auf dynamischem Puffer SRV angezeigt wird

<span id="SUMMARYINFO_MultisampleRTVWithForcedSampleCountOne"></span><span id="summaryinfo_multisamplertvwithforcedsamplecountone"></span><span id="SUMMARYINFO_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE"></span>**SUMMARYINFO \_ MultisampleRTVWithForcedSampleCountOne**  
Im vsglog-Beispiel angezeigter Text Eigenschaftenfenster – Multisample RTV with Forced Sample Count One

<span id="SUMMARYINFO_SAD4ShaderInstructions"></span><span id="summaryinfo_sad4shaderinstructions"></span><span id="SUMMARYINFO_SAD4SHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ SAD4ShaderInstructions**  
Text, der im vsglog-Eigenschaftenfenster – SAD4-Shaderanweisungen angezeigt wird

<span id="SUMMARYINFO_ExtendedDoublesShaderInstructions"></span><span id="summaryinfo_extendeddoublesshaderinstructions"></span><span id="SUMMARYINFO_EXTENDEDDOUBLESSHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ ExtendedDoublesShaderInstructions**  
Text, der im vsglog-Eigenschaftenfenster - Extended Doubles Shader Instructions (Anweisungen zum erweiterten Doubles-Shader) angezeigt wird

<span id="SUMMARYINFO_ExtendedResourceSharing"></span><span id="summaryinfo_extendedresourcesharing"></span><span id="SUMMARYINFO_EXTENDEDRESOURCESHARING"></span>**SUMMARYINFO \_ ExtendedResourceSharing**  
Text, der im vsglog-Eigenschaftenfenster – Erweiterte Ressourcenfreigabe angezeigt wird

<span id="SUMMARYINFO_D3D11_FEATURE_ARCHITECTURE_INFO"></span><span id="summaryinfo_d3d11_feature_architecture_info"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ ARCHITECTURE \_ INFO**  
Text im VSGLOG-Eigenschaftenfenster – D3D11 \_ FEATURE \_ ARCHITECTURE \_ INFO

<span id="SUMMARYINFO_TileBasedDeferredRenderer"></span><span id="summaryinfo_tilebaseddeferredrenderer"></span><span id="SUMMARYINFO_TILEBASEDDEFERREDRENDERER"></span>**SUMMARYINFO \_ TileBasedDeferredRenderer**  
Text, der im vsglog-Eigenschaftenfenster - Tile Based Deferred Renderer (Auf Kacheln basierender verzögerter Renderer) angezeigt wird

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d9_options"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D9 \_ OPTIONS**  
Text im vsglog-Eigenschaftenfenster – D3D11 \_ FEATURE \_ D3D9 \_ OPTIONS

<span id="SUMMARYINFO_FullNonPow2TextureSupport"></span><span id="summaryinfo_fullnonpow2texturesupport"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORT"></span>**SUMMARYINFO \_ FullNonPow2TextureSupport**  
Text, der im vsglog-Eigenschaftenfenster - Full Non-Pow2 Texture Support (Vollständige Texturunterstützung ohne Pow2) angezeigt wird

<span id="SUMMARYINFO_D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT"></span><span id="summaryinfo_d3d11_feature_shader_min_precision_support"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ SHADER \_ MIN \_ PRECISION \_ SUPPORT**  
Text, der im vsglog-Eigenschaftenfenster – D3D11 \_ FEATURE \_ SHADER \_ MIN PRECISION \_ \_ SUPPORT

<span id="SUMMARYINFO_PixelShaderMinPrecision"></span><span id="summaryinfo_pixelshaderminprecision"></span><span id="SUMMARYINFO_PIXELSHADERMINPRECISION"></span>**SUMMARYINFO \_ PixelShaderMinPrecision**  
Im Vsglog angezeigter Text Eigenschaftenfenster – Pixel-Shader– Mindestgenauigkeit

<span id="SUMMARYINFO_AllOtherShaderStagesMinPrecision"></span><span id="summaryinfo_allothershaderstagesminprecision"></span><span id="SUMMARYINFO_ALLOTHERSHADERSTAGESMINPRECISION"></span>**SUMMARYINFO \_ AllOtherShaderStagesMinPrecision**  
Im Vsglog angezeigter Text Eigenschaftenfenster – Alle anderen Shaderstufen– Mindestgenauigkeit

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SHADOW_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_shadow_support"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D9 \_ SHADOW \_ SUPPORT**  
Text im VSGLOG-Eigenschaftenfenster – D3D11 \_ FEATURE \_ D3D9 \_ SHADOW \_ SUPPORT

<span id="SUMMARYINFO_SupportsDepthAsTextureWithLessEqualComparisonFilter"></span><span id="summaryinfo_supportsdepthastexturewithlessequalcomparisonfilter"></span><span id="SUMMARYINFO_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER"></span>**SUMMARYINFO \_ SupportsDepthAsTextureWithLessEqualComparisonFilter**  
Text, der im vsglog-Eigenschaftenfenster angezeigt wird: Unterstützt Depth as Texture with Less Equal Comparison Filter (Tiefe als Textur mit weniger gleich einem Vergleichsfilter)

<span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d11_options1"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS1**  
Text im vsglog-Eigenschaftenfenster – D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS1

<span id="SUMMARYINFO_TiledResourcesTier"></span><span id="summaryinfo_tiledresourcestier"></span><span id="SUMMARYINFO_TILEDRESOURCESTIER"></span>**SUMMARYINFO \_ TiledResourcesTier**  
Text, der im vsglog-Eigenschaftenfenster – Ebene "Gekachelte Ressourcen" angezeigt wird

<span id="SUMMARYINFO_MinMaxFiltering"></span><span id="summaryinfo_minmaxfiltering"></span><span id="SUMMARYINFO_MINMAXFILTERING"></span>**SUMMARYINFO \_ MinMaxFiltering**  
Im vsglog-Text angezeigter text Eigenschaftenfenster – Min Max Filtering

<span id="SUMMARYINFO_ClearViewAlsoSupportsDepthOnlyFormats"></span><span id="summaryinfo_clearviewalsosupportsdepthonlyformats"></span><span id="SUMMARYINFO_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS"></span>**SUMMARYINFO \_ ClearViewAlsoSupportsDepthOnlyFormats**  
Text, der im vsglog-Eigenschaftenfenster - Clear View angezeigt wird, unterstützt auch nur Tiefenformate.

<span id="SUMMARYINFO_MapOnDefaultBuffers"></span><span id="summaryinfo_mapondefaultbuffers"></span><span id="SUMMARYINFO_MAPONDEFAULTBUFFERS"></span>**SUMMARYINFO \_ MapOnDefaultBuffers**  
Text, der im vsglog-Eigenschaftenfenster – Zuordnung zu Standardpuffern angezeigt wird

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_simple_instancing_support"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D9 \_ SIMPLE \_ INSTANCING \_ SUPPORT**  
Text, der im VSGLOG-Eigenschaftenfenster – D3D11 \_ FEATURE \_ D3D9 \_ SIMPLE \_ INSTANCING \_ SUPPORT

<span id="SUMMARYINFO_SimpleInstancingSupported0"></span><span id="summaryinfo_simpleinstancingsupported0"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED0"></span>**SUMMARYINFO \_ SimpleInstancingSupported0**  
Text, der im vsglog-Eigenschaftenfenster – Simple Instancing Supported 0 (Einfache Instancing unterstützt 0) angezeigt wird

<span id="SUMMARYINFO_D3D11_FEATURE_MARKER_SUPPORT"></span><span id="summaryinfo_d3d11_feature_marker_support"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE MARKER SUPPORT (FEATUREMARKERUNTERSTÜTZUNG FÜR SUMMARYINFO D3D11) \_ \_**  
Text, der im VSGLOG-Eigenschaftenfenster – D3D11 \_ FEATURE \_ MARKER \_ SUPPORT

<span id="SUMMARYINFO_Profile"></span><span id="summaryinfo_profile"></span><span id="SUMMARYINFO_PROFILE"></span>**\_SUMMARYINFO-Profil**  
Im vsglog-Profil Eigenschaftenfenster angezeigter Text

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d9_options1"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D9 \_ OPTIONS1**  
Text im vsglog-Eigenschaftenfenster – D3D11 \_ FEATURE \_ D3D9 \_ OPTIONS1

<span id="SUMMARYINFO_FullNonPow2TextureSupported"></span><span id="summaryinfo_fullnonpow2texturesupported"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORTED"></span>**SUMMARYINFO \_ FullNonPow2TextureSupported**  
Text, der im vsglog-Eigenschaftenfenster – Vollständige Nicht-Pow2-Textur unterstützt

<span id="SUMMARYINFO_DepthAsTextureWithLessEqualComparisonFilterSupported"></span><span id="summaryinfo_depthastexturewithlessequalcomparisonfiltersupported"></span><span id="SUMMARYINFO_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED"></span>**SUMMARYINFO \_ DepthAsTextureWithLessEqualComparisonFilterSupported**  
Im vsglog-Beispiel angezeigter Text Eigenschaftenfenster - Depth As Texture with Less Equal Comparison Filter Supported

<span id="SUMMARYINFO_SimpleInstancingSupported1"></span><span id="summaryinfo_simpleinstancingsupported1"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED1"></span>**SUMMARYINFO \_ SimpleInstancingSupported1**  
Text, der im vsglog-Eigenschaftenfenster – Simple Instancing Supported 1

<span id="SUMMARYINFO_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported"></span><span id="summaryinfo_texturecubefacerendertargetwithnoncubedepthstencilsupported"></span><span id="SUMMARYINFO_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED"></span>**SUMMARYINFO \_ TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported**  
Text, der im vsglog-Eigenschaftenfenster – Renderziel für Texturcube-Gesichtserkennung mit unterstützter Nicht-Cube-Tiefen-Schablone angezeigt wird

<span id="SUMMARYINFO_DXGIFormat"></span><span id="summaryinfo_dxgiformat"></span><span id="SUMMARYINFO_DXGIFORMAT"></span>**SUMMARYINFO \_ DXGIFormat**  
Im vsglog-Beispiel angezeigter Text Eigenschaftenfenster DXGIFormat

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
Im Dialogfeld "Firewall konfigurieren" angezeigter Text – Konfigurierte Textfirewall

<span id="IDS_FIREWALL_RULE_NAME"></span><span id="ids_firewall_rule_name"></span>**NAME DER \_ IDS-FIREWALLREGEL \_ \_**  
Text, der im Dialogfeld Firewall konfigurieren – Name der Firewallregel angezeigt wird

<span id="IDS_FIREWALL_RULE_DESCRIPTION"></span><span id="ids_firewall_rule_description"></span>**BESCHREIBUNG DER \_ \_ IDS-FIREWALLREGEL \_**  
Text im Dialogfeld "Firewall konfigurieren" – Beschreibung der Firewallregel

<span id="IDS_STATIC_HEADER"></span><span id="ids_static_header"></span>**STATISCHER \_ \_ IDS-HEADER**  
Text im Dialogfeld "Firewall konfigurieren" – Statischer Header

<span id="IDS_CONFIGURATION_TITLE"></span><span id="ids_configuration_title"></span>**\_IDS-KONFIGURATIONSTITEL \_**  
Im Dialogfeld "Firewall konfigurieren" – Konfigurationstitel angezeigter Text

<span id="IDS_STATIC_FW_HEADER"></span><span id="ids_static_fw_header"></span>**STATISCHER \_ \_ IDS-FW-HEADER \_**  
Im Dialogfeld Firewall konfigurieren – Statischer Firewallheader angezeigter Text

<span id="IDS_STATIC_GROUPBOX_FW"></span><span id="ids_static_groupbox_fw"></span>**IDS \_ STATIC \_ GROUPBOX \_ FW**  
Im Dialogfeld Firewall konfigurieren – Statische Groupbox-Firewall angezeigter Text

<span id="IDS_CHECK_FW_DOMAIN_NETWORKS"></span><span id="ids_check_fw_domain_networks"></span>**IDS \_ CHECK \_ FW \_ DOMAIN \_ NETWORKS**  
Text im Dialogfeld "Firewall konfigurieren" – Überprüfen von Firewalldomänennetzwerken

<span id="IDS_CHECK_FW_PRIVATE_NETWORKS"></span><span id="ids_check_fw_private_networks"></span>**IDS \_ CHECK \_ FW \_ PRIVATE \_ NETWORKS**  
Text im Dialogfeld "Firewall konfigurieren" – Überprüfen privater Firewallnetzwerke

<span id="IDS_CHECK_FW_PUBLIC_NETWORKS"></span><span id="ids_check_fw_public_networks"></span>**IDS \_ CHECK \_ FW \_ PUBLIC \_ NETWORKS**  
Text im Dialogfeld "Firewall konfigurieren" – Überprüfen der öffentlichen Firewallnetzwerke

<span id="IDS_BUTTON_CONFIGURE"></span><span id="ids_button_configure"></span>**IDS \_ BUTTON CONFIGURE (IDS-SCHALTFLÄCHE \_ KONFIGURIEREN)**  
Text im Dialogfeld "Firewall konfigurieren" – Buttom-Konfiture

<span id="IDS_CONFIGURATION_CANCEL"></span><span id="ids_configuration_cancel"></span>**\_IDS-KONFIGURATION \_ ABBRECHEN**  
Im Dialogfeld "Firewall konfigurieren" angezeigter Text– Konfigurations abbrechen

<span id="IDS_CAPTURETOOLTIP_MESSAGE_CORESYSTEM"></span><span id="ids_capturetooltip_message_coresystem"></span>**IDS \_ CAPTURETOOLTIP \_ MESSAGE \_ CORESYSTEM**  
Ressourcen-ID für die Zeichenfolge "Use the capture button in Visual Studio to capture frame(s)".

<span id="IDS_ET_NONE"></span><span id="ids_et_none"></span>**IDS \_ ET \_ NONE**  
Nicht verwendet.

<span id="IDS_ET_SESSIONSTART"></span><span id="ids_et_sessionstart"></span>**IDS \_ ET \_ SESSIONSTART**  
Nicht verwendet.

<span id="IDS_ET_SESSIONEND"></span><span id="ids_et_sessionend"></span>**IDS \_ ET \_ SESSIONEND**  
Nicht verwendet.

<span id="IDS_ET_PROCESSSTART"></span><span id="ids_et_processstart"></span>**IDS \_ ET \_ PROCESSSTART**  
Nicht verwendet.

<span id="IDS_ET_PROCESSEND"></span><span id="ids_et_processend"></span>**IDS \_ ET \_ PROCESSEND**  
Nicht verwendet.

<span id="IDS_ET_FRAMEBEGIN"></span><span id="ids_et_framebegin"></span>**IDS \_ ET \_ FRAMEBEGIN**  
Nicht verwendet.

<span id="IDS_ET_FRAMEEND"></span><span id="ids_et_frameend"></span>**IDS \_ ET \_ FRAMEEND**  
Nicht verwendet.

<span id="IDS_ET_USEREVENTBEGIN"></span><span id="ids_et_usereventbegin"></span>**IDS \_ ET \_ USEREVENTBEGIN**  
Nicht verwendet.

<span id="IDS_ET_USEREVENTEND"></span><span id="ids_et_usereventend"></span>**IDS \_ ET \_ USEREVENTEND**  
Nicht verwendet.

<span id="IDS_ET_USERMARKER"></span><span id="ids_et_usermarker"></span>**IDS \_ ET \_ USERMARKER**  
Nicht verwendet.

<span id="IDS_ET_CALL"></span><span id="ids_et_call"></span>**IDS \_ ET \_ CALL**  
Nicht verwendet.

<span id="IDS_ET_OBJECTPOPULATION"></span><span id="ids_et_objectpopulation"></span>**IDS \_ ET \_ OBJECTPOPULATION**  
Nicht verwendet.

<span id="IDS_ET_OBJECTCREATION"></span><span id="ids_et_objectcreation"></span>**IDS \_ ET \_ OBJECTCREATION**  
Nicht verwendet.

<span id="IDS_ET_CALLSYNC"></span><span id="ids_et_callsync"></span>**IDS \_ ET \_ CALLSYNC**  
Nicht verwendet.

<span id="IDS_ET_UNKNOWN"></span><span id="ids_et_unknown"></span>**IDS \_ ET \_ UNKNOWN**  
Nicht verwendet.

<span id="IDS_TRIGGER_NONE"></span><span id="ids_trigger_none"></span>**IDS \_ TRIGGER \_ NONE**  
Nicht verwendet.

<span id="IDS_TRIGGER_PROGRAMSTART"></span><span id="ids_trigger_programstart"></span>**IDS \_ TRIGGER \_ PROGRAMSTART**  
Nicht verwendet.

<span id="IDS_TRIGGER_FRAME"></span><span id="ids_trigger_frame"></span>**\_IDS-TRIGGERFRAME \_**  
Nicht verwendet.

<span id="IDS_TRIGGER_TIME"></span><span id="ids_trigger_time"></span>**\_IDS-TRIGGERZEIT \_**  
Nicht verwendet.

<span id="IDS_TRIGGER_USERMARKER"></span><span id="ids_trigger_usermarker"></span>**IDS \_ TRIGGER \_ USERMARKER**  
Nicht verwendet.

<span id="IDS_TRIGGER_BEGINUSEREVENT"></span><span id="ids_trigger_beginuserevent"></span>**IDS \_ TRIGGER \_ BEGINUSEREVENT**  
Nicht verwendet.

<span id="IDS_TRIGGER_ENDUSEREVENT"></span><span id="ids_trigger_enduserevent"></span>**IDS \_ TRIGGER \_ ENDUSEREVENT**  
Nicht verwendet.

<span id="IDS_TRIGGER_CAPTUREFRAME"></span><span id="ids_trigger_captureframe"></span>**IDS \_ TRIGGER \_ CAPTUREFRAME**  
Nicht verwendet.

<span id="IDS_TRIGGER_APICAPTURE"></span><span id="ids_trigger_apicapture"></span>**IDS \_ TRIGGER \_ APICAPTURE**  
Nicht verwendet.

<span id="IDS_ERROR_CALLDATA"></span><span id="ids_error_calldata"></span>**\_IDS-FEHLER \_ CALLDATA**  
Nicht verwendet.

<span id="IDS_ERROR_CREATINGLOG"></span><span id="ids_error_creatinglog"></span>**\_IDS-FEHLER \_ CREATINGLOG**  
Nicht verwendet.

<span id="IDS_UNKNOWNCALL"></span><span id="ids_unknowncall"></span>**IDS \_ UNKNOWNCALL**  
Nicht verwendet.

<span id="IDS_WARN_FEATURE_LEVEL_CHANGED"></span><span id="ids_warn_feature_level_changed"></span>**IDS \_ \_ WARNFUNKTIONSEBENE \_ \_ GEÄNDERT**  
Nicht verwendet.

<span id="ID_STATUS_FREQUENCY"></span><span id="id_status_frequency"></span>**\_ \_ ID-STATUSHÄUFIGKEIT**  

<span id="ID_DISABLE_HUD"></span><span id="id_disable_hud"></span>**ID \_ DISABLE \_ HUD**  

<span id="ID_DISABLE_COMPAT"></span><span id="id_disable_compat"></span>**ID \_ DISABLE \_ COMPAT**  

<span id="ID_COLLECT_CALLSTACKS"></span><span id="id_collect_callstacks"></span>**ID \_ COLLECT \_ CALLSTACKS**  

<span id="ID_ENABLE_SDKERROR_STOP"></span><span id="id_enable_sdkerror_stop"></span>**ID: \_ \_ SDKERROR BEENDEN \_ AKTIVIEREN**  

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



