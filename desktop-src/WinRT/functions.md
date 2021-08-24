---
description: Ein Verweis auf Windows Runtime-C++-Funktionen.
ms.assetid: 3D60C81F-B1CC-4485-B7C3-B1C6E903865B
title: Funktionen (Windows Runtime)
ms.topic: article
ms.date: 05/10/2019
ms.openlocfilehash: fbf0d4ce350251e1c13d1f6a3ff03c95068558098eac722979bc77499a094c4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795010"
---
# <a name="functions-windows-runtime-c-reference"></a>Funktionen (C++-Referenz Windows Runtime)

## <a name="in-this-section"></a>In diesem Abschnitt



| Funktion | Beschreibung |
|-|-|
| [**CoDecodeProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-codecodeproxy) | Sucht die Implementierung einer COM-Schnittstelle (Component Object Model) in einem Serverprozess, wenn eine Schnittstelle zu einem Proxieobjekt vorhanden ist. |
| [**CreateControlInput**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinput) | Erstellt ein [**ICoreInputSourceBase-Objekt**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) im UI-Thread des Aufrufers. |
| [**CreateControlInputEx**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinputex) | Erstellt ein [**ICoreInputSourceBase-Objekt**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) in einem Arbeitsthread oder ui-Thread.  |
| [**CreateDirect3D11DeviceFromDXGIDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11devicefromdxgidevice) | Erstellt eine Instanz von IDirect3DDevice aus einem IDXGIDevice. |
| [**CreateDirect3D11SurfaceFromDXGISurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11surfacefromdxgisurface) | Erstellt eine Instanz von IDirect3DSurface aus einer IDXGISurface. |
| [**CreateDirect3DDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3ddevice) | Erstellt eine Instanz von [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) aus einem [IDXGIDevice](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)-Objekt. |
| [**CreateDirect3DSurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3dsurface) | Erstellt eine Instanz von [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) aus einem [IDXGISurface](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface)-Objekt. |
| [**CreateRandomAccessStreamOnFile**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamonfile) | Erstellt einen Windows Runtime-Datenstrom für zufälligen Zugriff für eine Datei. |
| [**CreateRandomAccessStreamOverStream**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamoverstream) | Erstellt einen Windows Runtime-Datenstrom für [](/windows/win32/api/objidl/nn-objidl-istream) zufälligen Zugriff um eine IStream-Basisimplementierungen. |
| [**CreateStreamOverRandomAccessStream**](/windows/win32/api/shcore/nf-shcore-createstreamoverrandomaccessstream) | Erstellt einen [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) um ein Windows [**Runtime-IRandomAccessStream-Objekt.**](/previous-versions//hh438400(v=vs.85)) |
| [**CreateXamlUIPresenter**](createxamluipresenter.md) | Eine statische Erstellerfunktion, die einen [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) für eine Renderoberfläche in einer Desktop-App erstellen kann. |
| [**DbgRtraktionAssertionFailure**](/previous-versions//jj635749(v=vs.85)) | Löst eine Assertion für das Debuggen aus.  |
| [**GetDXGIInterface(IDirect3DDevice^, DXGI_TYPE**)**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface) | Ruft eine DXGI-Schnittstelle aus einer [IDirect3DDevice-Instanz](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) ab. |
| [**GetDXGIInterface(IDirect3DSurface^, DXGI_TYPE**)**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface-r1) | Ruft eine DXGI-Schnittstelle aus einer [IDirect3DSurface-Instanz](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) ab. |
| [**GetDXGIInterfaceFromObject**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterfacefromobject) | Ruft eine DXGI-Schnittstelle aus einem -Objekt ab. |
| [**GetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-getrestrictederrorinfo) | Ruft das eingeschränkte Fehlerinformationsobjekt ab, das durch einen vorherigen Aufruf von [**SetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) im aktuellen logischen Thread festgelegt wurde. |
| [**HSTRING \_ UserFree**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree) | Gibt Ressourcen auf Serverseite frei, wenn sie von RPC-Stubdateien aufgerufen werden. |
| [**HSTRING \_ UserFree64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree64) | Gibt Ressourcen auf Serverseite frei, wenn sie von RPC-Stubdateien aufgerufen werden.  |
| [**HSTRING \_ UserMarshal**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal) | Marshallt ein [**HSTRING-Objekt**](hstring.md) in den RPC-Puffer. |
| [**HSTRING \_ UserMarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal64) | Marshallt ein [**HSTRING-Objekt**](hstring.md) in den RPC-Puffer. |
| [**HSTRING \_ UserSize**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize) | Berechnet die Kabelgröße des [**HSTRING-Objekts**](hstring.md) und ruft dessen Handle und Daten ab. |
| [**HSTRING \_ UserSize64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize64) | Berechnet die Kabelgröße des [**HSTRING-Objekts**](hstring.md) und ruft dessen Handle und Daten ab. |
| [**HSTRING \_ UserUnmarshal**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal) | Entfernt ein [**HSTRING-Objekt**](hstring.md) aus dem RPC-Puffer. |
| [**HSTRING \_ UserUnmarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal64) | Entfernt ein [**HSTRING-Objekt**](hstring.md) aus dem RPC-Puffer. |
| [**IsErrorPropagationEnabled**](/windows/win32/api/roerrorapi/nf-roerrorapi-iserrorpropagationenabled) | Gibt an, ob das [**CoreApplication.UnhandledErrorDetected-Ereignis**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) für die Fehler auftritt, die vom Delegaten zurückgegeben werden, der als Rückruffunktion für ein Windows Runtime-API-Ereignis registriert ist, oder den Abschluss einer asynchronen Methode. |
| [**DllGetActivationFactory**](/previous-versions//br205771(v=vs.85)) | Ruft die Aktivierungsfactory aus einer DLL ab, die aktivierbare Windows Laufzeitklassen enthält. |
| [**MetaDataGetDispenser**](/windows/win32/api/rometadata/nf-rometadata-metadatagetdispenser) | Erstellt eine Verteilerklasse. |
| [**PdfCreateRenderer**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfcreaterenderer) | Ruft eine Instanz der [**IPdfRendererNative-Schnittstelle**](/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative) zum Anzeigen einer einzelnen Seite einer PDF-Datei (Portable Document Format) ab. |
| [**PdfRenderParams**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfrenderparams) | Füllt eine [**\_ \_ PDF-RENDER-PARAMS-Stucture**](/windows/desktop/api/windows.data.pdf.interop/ns-windows-data-pdf-interop-pdf_render_params) auf. Eine PDF \_ RENDER \_ PARAMS-Struktur stellt eine Reihe von Eigenschaften zum Ausgeben einer einzelnen Seite einer PDF-Datei dar. |
| [**RoActivateInstance**](/windows/win32/api/roapi/nf-roapi-roactivateinstance) | Aktiviert die angegebene Windows Runtime-Klasse. |
| [**RoCaptureErrorContext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext) | Speichert den aktuellen Fehlerkontext, damit er für spätere Aufrufe der [**RoFailFastWithErrorContext-Funktion**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) verfügbar ist. |
| [**RoClearError**](/windows/win32/api/roerrorapi/nf-roerrorapi-roclearerror) | Entfernt vorhandene Fehlerinformationen aus dem aktuellen Threadumgebungsblock (TEB). |
| [**RoFailFastWithErrorContext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) | Löst eine nicht zusammenhängende Ausnahme im aktuellen Prozess aus. |
| [**RoFailFastWithErrorContextInternal2**](./roerrorapi/nf-roerrorapi-rofailfastwitherrorcontextinternal2.md) | Löst eine nicht zusammenhängende Ausnahme im aktuellen Prozess aus und ermöglicht es Ihnen auch, zusätzliche Fehlerkontexte einzuschließen, die nicht bereits vom Betriebssystem erfasst wurden. |
| [**RoFreeParameterizedTypeExtra**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rofreeparameterizedtypeextra) | Gibt das von [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid)zugeordnete Handle frei. |
| [**RoGetActivatableClassRegistration**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration) | Ermöglicht das Abrufen von Klassenregistrierungsinformationen. |
| [**RoGetActivationFactory**](/windows/win32/api/roapi/nf-roapi-rogetactivationfactory) | Ruft die Aktivierungsfactory für die angegebene Laufzeitklasse ab. |
| [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) | Erstellt einen agilen Verweis für ein objekt, das von der angegebenen Schnittstelle angegeben wird. |
| [**RoGetApartmentIdentifier**](/windows/win32/api/roapi/nf-roapi-rogetapartmentidentifier) | Ruft einen eindeutigen Bezeichner für das aktuelle Apartment ab. |
| [**RoGetBufferMarshaler**](/windows/win32/api/robuffer/nf-robuffer-rogetbuffermarshaler) | Stellt einen Standardmäßig-IBuffer-Marshaller bereit, um die Semantik zu implementieren, die der IBuffer-Schnittstelle zugeordnet ist, wenn sie gemarshallt wird. |
| [**RoGetErrorReportingFlags**](/windows/win32/api/roerrorapi/nf-roerrorapi-rogeterrorreportingflags) | Ruft das aktuelle Berichtsverhalten von Windows Runtime-Fehlerfunktionen ab. |
| [**RoGetMetaDataFile**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-rogetmetadatafile) | Sucht die Metadatendatei, die die Application Binary Interface (ABI) für den angegebenen Typnamen beschreibt, und ruft sie ab. |
| [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) | Berechnet den Schnittstellenbezeichner (IID) des Schnittstellen- oder Delegattyps, der sich ergibt, wenn eine parametrisierte Schnittstelle oder ein Delegat mit den angegebenen Typargumenten instanziiert wird. |
| [**RoGetServerActivatableClasses**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetserveractivatableclasses) | Ruft die aktivierbaren Klassen ab, die für einen bestimmten ausführbaren Server (EXE) registriert sind, der unter der Paket-ID des aufrufenden Prozesses registriert wurde. |
| [**RoInitialize**](/windows/win32/api/roapi/nf-roapi-roinitialize) | Initialisiert die Windows Runtime im aktuellen Thread mit dem angegebenen Parallelitätsmodell. |
| [**RoInspectThreadErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectthreaderrorinfo) | Ruft das Fehlerobjekt ab, das die Aufrufliste an dem Punkt darstellt, an dem der Fehler aufgetreten ist. |
| [**RoInspectCapturedStackBackTrace**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectcapturedstackbacktrace) | Bietet Debuggern die Möglichkeit, eine Aufrufliste aus einem Zielprozess zu untersuchen. |
| [**RoOriginateError**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerror) | Meldet einen Fehler und eine informative Zeichenfolge an einen angefügten Debugger. |
| [**RoOriginateErrorW**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerrorw) | Meldet einen Fehler und eine informative Zeichenfolge an einen angefügten Debugger. |
| [**RoOriginateLanguageException**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginatelanguageexception) | Meldet einen Fehler, eine informative Zeichenfolge und ein Fehlerobjekt an einen angefügten Debugger. |
| [**RoParameterizedTypeExtraGetTypeSignature**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-roparameterizedtypeextragettypesignature) | Ruft die Typsignatur ab, die zum Berechnen der IID aus dem letzten Aufruf von [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) mit dem angegebenen Handle verwendet wird. |
| [**RoParseTypeName**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roparsetypename) | Analysiert einen Typnamen und vorhandene Typparameter im Fall parametrisierte Typen. |
| [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) | Registriert eine Out-of-Process-Aktivierungs factorys eines Arrays für einen Windows Runtime-EXE-Server. |
| [**RoRegisterForApartmentShutdown**](/windows/win32/api/roapi/nf-roapi-roregisterforapartmentshutdown) | Registriert einen [**IApartmentShutdown-Rückruf,**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) der aufgerufen wird, wenn das aktuelle Apartment heruntergefahren wird. |
| [**RoReportUnhandledError**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportunhandlederror) | Löst den globalen Fehlerhandler aus, wenn eine nicht behandelte Ausnahme auftritt. |
| [**RoReportFailedDelegate**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportfaileddelegate) | Löst den globalen Fehlerhandler aus, wenn ein Delegatfehler auftritt. |
| [**RoResolveNamespace**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roresolvenamespace) | Bestimmen Sie die direkten untergeordneten, typen und untergeordneten Namespaces des angegebenen Windows Runtime-Namespace aus jeder Programmiersprache, die von der Windows Runtime unterstützt wird. |
| [**RoResolveRestrictedErrorInfoReference**](/windows/win32/api/roerrorapi/nf-roerrorapi-roresolverestrictederrorinforeference) | Gibt den [**IRestrictedErrorInfo-Schnittstellenzeiger**](/windows/desktop/api/RestrictedErrorInfo/nn-restrictederrorinfo-irestrictederrorinfo) basierend auf dem angegebenen Verweis zurück. |
| [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) | Entfernt ein Array registrierter Aktivierungs factorys aus der Windows Runtime. |
| [**RoSetErrorReportingFlags**](/windows/win32/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags) | Legt das Berichterstellungsverhalten von Windows Runtime-Fehlerfunktionen fest. |
| [**RoTransformError**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerror) | Meldet einen geänderten Fehler und eine informative Zeichenfolge an einen angefügten Debugger. |
| [**RoTransformErrorW**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerrorw) | Meldet einen transformierten Fehler und eine informative Zeichenfolge an einen angefügten Debugger. |
| [**RoUninitialize**](/windows/win32/api/roapi/nf-roapi-rouninitialize) | Schließt die Windows Runtime für den aktuellen Thread. |
| [**RoUnregisterForApartmentShutdown**](/windows/win32/api/roapi/nf-roapi-rounregisterforapartmentshutdown) | Aufheben der Registrierung einer zuvor registrierten [**IApartmentShutdown-Schnittstelle.**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) |
| [**SetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) | Legt das Eingeschränkte Fehlerinformationsobjekt für den aktuellen Thread fest. |
| [**WindowsCompareStringOrdinal**](/windows/win32/api/winstring/nf-winstring-windowscomparestringordinal) | Vergleicht zwei angegebene [**HSTRING-Objekte**](hstring.md) und gibt eine ganze Zahl zurück, die ihre relative Position in einer Sortierreihenfolge angibt. |
| [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) | Verkettet zwei angegebene Zeichenfolgen. |
| [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) | Erstellt eine neue [**HSTRING-Datei**](hstring.md) basierend auf der angegebenen Quellzeichenfolge. |
| [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) | Erstellt einen neuen Zeichenfolgenverweis basierend auf der angegebenen Zeichenfolge. |
| [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) | Dekrementiert die Verweisanzahl eines Zeichenfolgenpuffers. |
| [**WindowsDeleteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowsdeletestringbuffer) | Verwirft einen vorab zugewiesenen Zeichenfolgenpuffer, wenn er nicht zu einem [**HSTRING -Wert promotet wurde.**](hstring.md) |
| [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) | Erstellt eine Kopie der angegebenen Zeichenfolge. |
| [**WindowsGetStringLen**](/windows/win32/api/winstring/nf-winstring-windowsgetstringlen) | Ruft die Länge der angegebenen Zeichenfolge in Unicode-Zeichen ab. |
| [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) | Ruft den Hintergrundpuffer für die angegebene Zeichenfolge ab. |
| [**WindowsInspectString**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring) | Bietet Debuggern die Möglichkeit, den Wert eines Windows Runtime [**HSTRING**](hstring.md) in einem anderen Adressraum, remote oder aus einem Speicherabbild anzuzeigen.  |
| [**WindowsInspectString2**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring2) | Bietet Debuggern die Möglichkeit, den Wert eines Windows Runtime [**HSTRING**](hstring.md) in einem anderen Adressraum, remote oder aus einem Speicherabbild anzuzeigen.  |
| [**WindowsIsStringEmpty**](/windows/win32/api/winstring/nf-winstring-windowsisstringempty) | Gibt an, ob die angegebene Zeichenfolge die leere Zeichenfolge ist. |
| [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) | Ordnet einen veränderlichen Zeichenpuffer für die Verwendung bei der [**HSTRING-Erstellung**](hstring.md) zu. |
| [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) | Erstellt eine [**HSTRING-Datei**](hstring.md) aus dem [**angegebenen HSTRING \_ BUFFER.**](hstring-buffer.md) |
| [**WindowsReplaceString**](/windows/win32/api/winstring/nf-winstring-windowsreplacestring) | Ersetzt alle Vorkommen eines Zeichensets in der angegebenen Zeichenfolge durch einen anderen Satz von Zeichen, um eine neue Zeichenfolge zu erstellen. |
| [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) | Gibt an, ob die angegebene Zeichenfolge eingebettete NULL-Zeichen enthält. |
| [**WindowsSubstring**](/windows/win32/api/winstring/nf-winstring-windowssubstring) | Ruft eine Teilzeichenfolge aus der angegebenen Zeichenfolge ab. Die Teilzeichenfolge beginnt an der angegebenen Zeichenposition. |
| [**WindowsSubstringWithSpecifiedLength**](/windows/win32/api/winstring/nf-winstring-windowssubstringwithspecifiedlength) | Ruft eine Teilzeichenfolge aus der angegebenen Zeichenfolge ab. Die Teilzeichenfolge beginnt an einer angegebenen Zeichenposition und hat eine angegebene Länge. |
| [**WindowsTrimStringEnd**](/windows/win32/api/winstring/nf-winstring-windowstrimstringend) | Entfernt alle nachkommaenden Vorkommen eines angegebenen Zeichensets aus der Quellzeichenfolge. |
| [**WindowsTrimStringStart**](/windows/win32/api/winstring/nf-winstring-windowstrimstringstart) | Entfernt alle führenden Vorkommen eines angegebenen Zeichensets aus der Quellzeichenfolge. |



 

 

 
