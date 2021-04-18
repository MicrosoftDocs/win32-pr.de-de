---
description: Ein Verweis auf Windows-Runtime C++-Funktionen.
ms.assetid: 3D60C81F-B1CC-4485-B7C3-B1C6E903865B
title: Funktionen (Windows-Runtime)
ms.topic: article
ms.date: 05/10/2019
ms.openlocfilehash: 1ed2ea39385ac5cb7afc34770a5ee2d2a572bb8b
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106364508"
---
# <a name="functions-windows-runtime-c-reference"></a>Functions (Windows-Runtime C++-Referenz)

## <a name="in-this-section"></a>In diesem Abschnitt



| Funktion | BESCHREIBUNG |
|-|-|
| [**Codecodeproxy**](/windows/desktop/api/combaseapi/nf-combaseapi-codecodeproxy) | Gibt die Implementierung einer Component Object Model (com)-Schnittstelle in einem Server Prozess an, wenn eine Schnittstelle zu einem Proxy Objekt bereitgestellt wird. |
| [**"Kreatecontrolinput"**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinput) | Erstellt ein [**icoreinputsourcebase**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) -Objekt im UI-Thread des Aufrufers. |
| [**"Kreatecontrolinputex"**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinputex) | Erstellt ein [**icoreinputsourcebase**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) -Objekt in einem Arbeits Thread oder im UI-Thread.  |
| [**CreateDirect3D11DeviceFromDXGIDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11devicefromdxgidevice) | Erstellt eine Instanz von IDirect3DDevice von einem idxgidevice. |
| [**CreateDirect3D11SurfaceFromDXGISurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11surfacefromdxgisurface) | Erstellt eine Instanz von IDirect3DSurface aus einer idxgisurface. |
| [**CreateDirect3DDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3ddevice) | Erstellt eine Instanz von [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) von einem [idxgidevice](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice). |
| [**CreateDirect3DSurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3dsurface) | Erstellt eine Instanz von [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) aus einer [idxgisurface](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface). |
| [**"Kreaterandomaccessstreamonfile"**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamonfile) | Erstellt einen Windows-Runtime Random Access Stream für eine Datei. |
| [**"Kreaterandomaccessstreamoverstream"**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamoverstream) | Erstellt einen Windows-Runtime Random Access Stream um eine [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) -Basis Implementierung. |
| [**"Kreatestreamoverrandomaccessstream"**](/windows/win32/api/shcore/nf-shcore-createstreamoverrandomaccessstream) | Erstellt einen [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) um ein Windows-Runtime [**jeandomaccessstream**](/previous-versions//hh438400(v=vs.85)) -Objekt. |
| [**"Kreatexamluipresenter"**](createxamluipresenter.md) | Eine statische erstellerfunktion, die einen [**xamluipresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) für eine Renderoberfläche in einer Desktop-App erstellen kann. |
| [**Dbgraiseassertionfailure**](/previous-versions//jj635749(v=vs.85)) | Löst eine Bestätigung für das Debuggen aus.  |
| [**Getdxgiinterface (IDirect3DDevice ^, DXGI_TYPE**) * *](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface) | Ruft eine DXGI-Schnittstelle aus einer [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) -Instanz ab. |
| [**Getdxgiinterface (IDirect3DSurface ^, DXGI_TYPE**) * *](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface-r1) | Ruft eine DXGI-Schnittstelle aus einer [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) -Instanz ab. |
| [**Getdxgiinterfakefromuject**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterfacefromobject) | Ruft eine DXGI-Schnittstelle aus einem-Objekt ab. |
| [**Getrestrictederrorinfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-getrestrictederrorinfo) | Ruft das Objekt mit eingeschränkten Fehlerinformationen ab, das durch einen vorherigen aufrufenen [**setrestrictederrorinfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) -Befehl im aktuellen logischen Thread festgelegt wurde. |
| [**Hstring \_ userfree**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree) | Gibt Ressourcen auf der Serverseite frei, wenn Sie von RPC-Stub-Dateien aufgerufen werden. |
| [**Hstring \_ UserFree64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree64) | Gibt Ressourcen auf der Serverseite frei, wenn Sie von RPC-Stub-Dateien aufgerufen werden.  |
| [**Hstring \_ usermarshal**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal) | Marshunkt ein [**hstring**](hstring.md) -Objekt in den RPC-Puffer. |
| [**Hstring \_ UserMarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal64) | Marshunkt ein [**hstring**](hstring.md) -Objekt in den RPC-Puffer. |
| [**Hstring \_ usersize**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize) | Berechnet die Netzwerkgröße des [**hstring**](hstring.md) -Objekts und ruft dessen Handle und Daten ab. |
| [**Hstring \_ UserSize64**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize64) | Berechnet die Netzwerkgröße des [**hstring**](hstring.md) -Objekts und ruft dessen Handle und Daten ab. |
| [**Hstring \_ userunmarshal**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal) | Entfernt ein [**hstring**](hstring.md) -Objekt aus dem RPC-Puffer. |
| [**Hstring \_ UserUnmarshal64**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal64) | Entfernt ein [**hstring**](hstring.md) -Objekt aus dem RPC-Puffer. |
| [**Iserrorpropagationationaktivierte**](/windows/win32/api/roerrorapi/nf-roerrorapi-iserrorpropagationenabled) | Gibt an, ob das [**coreapplication. unhandlederrorfound**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) -Ereignis für die Fehler auftritt, die vom Delegaten zurückgegeben werden, der als Rückruffunktion für ein Windows-Runtime API-Ereignis oder den Abschluss einer asynchronen Methode registriert ist. |
| [**Dllgetactivationfactory**](/previous-versions//br205771(v=vs.85)) | Ruft die Aktivierungs Factory aus einer DLL ab, die aktivierbare Windows-Runtime Klassen enthält. |
| [**MetaDataGetDispenser**](/windows/win32/api/rometadata/nf-rometadata-metadatagetdispenser) | Erstellt eine Dispenser-Klasse. |
| [**Pdfkreatererderer**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfcreaterenderer) | Ruft eine Instanz der [**ipdfrenderernative**](/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative) -Schnittstelle ab, um eine einzelne Seite einer PDF-Datei (Portable Document Format) anzuzeigen. |
| [**Pdfrenderparameams**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfrenderparams) | Füllt eine [**PDF- \_ Rendering \_ -**](/windows/desktop/api/windows.data.pdf.interop/ns-windows-data-pdf-interop-pdf_render_params) parametriturstuktur auf. Eine PDF- \_ Rendering-parametrietstruktur \_ stellt einen Satz von Eigenschaften für die Ausgabe einer einzelnen Seite einer PDF-Datei dar. |
| [**Roactivateingestance**](/windows/win32/api/roapi/nf-roapi-roactivateinstance) | Aktiviert die angegebene Windows-Runtime-Klasse. |
| [**Rocaptureerrorcontext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext) | Speichert den aktuellen Fehler Kontext, sodass er für spätere Aufrufe der [**rofailfastwitherrorcontext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) -Funktion verfügbar ist. |
| [**Roclearerror**](/windows/win32/api/roerrorapi/nf-roerrorapi-roclearerror) | Entfernt vorhandene Fehlerinformationen aus dem aktuellen Thread Umgebungsblock (TEB). |
| [**Rofailfastwitherrorcontext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) | Löst im aktuellen Prozess eine nicht fort Setz Bare Ausnahme aus. |
| [**RoFailFastWithErrorContextInternal2**](./roerrorapi/nf-roerrorapi-rofailfastwitherrorcontextinternal2.md) | Löst im aktuellen Prozess eine nicht fort Setz Bare Ausnahme aus und ermöglicht es Ihnen außerdem, zusätzlichen Fehler Kontext einzuschließen, der noch nicht vom Betriebssystem erfasst wurde. |
| [**Rofreparameterizedtypeextra**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rofreeparameterizedtypeextra) | Gibt das von [**rogetparameterizedtypeinstanceiid**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid)zugewiesene Handle frei. |
| [**Rogetactivatableclassregistration**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration) | Ermöglicht das Abrufen von Klassen Registrierungsinformationen. |
| [**RoGetActivationFactory**](/windows/win32/api/roapi/nf-roapi-rogetactivationfactory) | Ruft die aktivierungsfactory für die angegebene Lauf Zeit Klasse ab. |
| [**Rogetagilereferenzierung**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) | Erstellt einen Agile-Verweis für ein Objekt, das von der angegebenen-Schnittstelle angegeben wird. |
| [**Rogetapartmentidentifier**](/windows/win32/api/roapi/nf-roapi-rogetapartmentidentifier) | Ruft einen eindeutigen Bezeichner für das aktuelle Apartment ab. |
| [**Rogetbuffermarshaler**](/windows/win32/api/robuffer/nf-robuffer-rogetbuffermarshaler) | Stellt einen standardmäßigen ibuffer-Mars Haller bereit, um die Semantik zu implementieren, die der ibuffer-Schnittstelle beim Marshalling zugeordnet ist. |
| [**Rogeterrorreportingflags**](/windows/win32/api/roerrorapi/nf-roerrorapi-rogeterrorreportingflags) | Ruft das aktuelle Berichts Verhalten Windows-Runtime Fehlerfunktionen ab. |
| [**RoGetMetaDataFile**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-rogetmetadatafile) | Sucht und ruft die Metadatendatei ab, die die Anwendungs Binärdatei Schnittstelle (ABI) für den angegebenen Typnamen beschreibt. |
| [**Rogetparameterizedtypeinstanceiid**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) | Berechnet den Schnittstellen Bezeichner (IID) der Schnittstelle oder des Delegattyps, der sich ergibt, wenn eine parametrisierte Schnittstelle oder ein Delegat mit den angegebenen Typargumenten instanziiert wird. |
| [**Rogetserveractivatableclasses**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetserveractivatableclasses) | Ruft die aktivierbaren Klassen ab, die für einen angegebenen ausführbaren Server (exe) registriert sind und unter der Paket-ID des aufrufenden Prozesses registriert wurden. |
| [**RoInitialize**](/windows/win32/api/roapi/nf-roapi-roinitialize) | Initialisiert die Windows-Runtime für den aktuellen Thread mit dem angegebenen Parallelitäts Modell. |
| [**Roinspectthreaderrorinfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectthreaderrorinfo) | Ruft das Fehler Objekt ab, das die Rückruf Stapel an dem Punkt darstellt, von dem der Fehler verursacht wurde. |
| [**Roinspectcapturedstackbacktrace**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectcapturedstackbacktrace) | Bietet eine Möglichkeit, von Debuggern eine Aufrufliste von einem Ziel Prozess zu überprüfen. |
| [**Rooriginateerror**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerror) | Meldet einen Fehler und eine informative Zeichenfolge an einen angefügten Debugger. |
| [**Rooriginateerrorw**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerrorw) | Meldet einen Fehler und eine informative Zeichenfolge an einen angefügten Debugger. |
| [**Rooriginatelanguageexception**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginatelanguageexception) | Meldet einen Fehler, eine informative Zeichenfolge und ein Fehler Objekt an einen angefügten Debugger. |
| [**Roparameterizedtypeextragettypeer Signature**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-roparameterizedtypeextragettypesignature) | Ruft die Typsignatur ab, mit der die IID aus dem letzten Aufrufen von [**rogetparameterizedtypeinstanceiid**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) mit dem angegebenen Handle berechnet wird. |
| [**Roparser-Typname**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roparsetypename) | Analysiert einen Typnamen und vorhandene Typparameter im Fall von parametrisierten Typen. |
| [**Roregisteractivationfactorys**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) | Registriert ein Array out-of-Process-Aktivierungs Factorys für einen Windows-Runtime exe-Server. |
| [**Roregisterforapartmentshutdown**](/windows/win32/api/roapi/nf-roapi-roregisterforapartmentshutdown) | Registriert einen [**iapartmentshutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) -Rückruf, der aufgerufen wird, wenn das aktuelle Apartment heruntergefahren wird. |
| [**Roreportunhandlederror**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportunhandlederror) | Löst den globalen Fehler Handler aus, wenn eine nicht behandelte Ausnahme auftritt. |
| [**Roreportfaileddelegat**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportfaileddelegate) | Löst den globalen Fehler Handler aus, wenn ein delegatfehler auftritt. |
| [**Roresolvenamespace**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roresolvenamespace) | Bestimmen Sie die direkten untergeordneten Elemente, Typen und Subnamespaces des angegebenen Windows-Runtime Namespace aus einer beliebigen Programmiersprache, die vom Windows-Runtime unterstützt wird. |
| [**Roresolverestrictederrorinforeferenzierung**](/windows/win32/api/roerrorapi/nf-roerrorapi-roresolverestrictederrorinforeference) | Gibt den [**irestrictederrorinfo**](/windows/desktop/api/RestrictedErrorInfo/nn-restrictederrorinfo-irestrictederrorinfo) -Schnittstellen Zeiger auf Grundlage des angegebenen Verweises zurück. |
| [**Rorevokeactivationfactorys**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) | Entfernt ein Array registrierter aktivierungfactorys aus dem Windows-Runtime. |
| [**Roseterrorreportingflags**](/windows/win32/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags) | Legt das Berichts Verhalten Windows-Runtime Fehlerfunktionen fest. |
| [**Rotransformerror**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerror) | Meldet einen geänderten Fehler und eine informative Zeichenfolge an einen angefügten Debugger. |
| [**Rotransformerrorw**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerrorw) | Meldet einen transformierten Fehler und eine informative Zeichenfolge an einen angefügten Debugger. |
| [**Rouninitialize**](/windows/win32/api/roapi/nf-roapi-rouninitialize) | Schließt die Windows-Runtime für den aktuellen Thread. |
| [**Rounregisterforapartmentshutdown**](/windows/win32/api/roapi/nf-roapi-rounregisterforapartmentshutdown) | Hebt die Registrierung einer zuvor registrierten [**iapartmentshutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) -Schnittstelle auf. |
| [**"Abtrestrictederrorinfo"**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) | Legt das Objekt mit eingeschränkten Fehlerinformationen für den aktuellen Thread fest. |
| [**Windowscomparestringordinal**](/windows/win32/api/winstring/nf-winstring-windowscomparestringordinal) | Vergleicht zwei angegebene [**hstring**](hstring.md) -Objekte und gibt eine ganze Zahl zurück, die ihre relative Position in einer Sortierreihenfolge angibt. |
| [**Windowsconcatstring**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) | Verkettet zwei angegebene Zeichen folgen. |
| [**Windowscreatestring**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) | Erstellt auf der Grundlage der angegebenen Quell Zeichenfolge einen neuen [**hstring**](hstring.md) . |
| [**Windowscreatestrauingreferenzierung**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) | Erstellt einen neuen Zeichen folgen Verweis auf der Grundlage der angegebenen Zeichenfolge. |
| [**Windowsdeletestring**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) | Dekremente den Verweis Zähler eines Zeichen folgen Puffers. |
| [**Windowsdeletestringbuffer**](/windows/win32/api/winstring/nf-winstring-windowsdeletestringbuffer) | Verwirft einen vorab zugeordneten Zeichen folgen Puffer, wenn er nicht zu einem [**hstring**](hstring.md)herauf gestuft wurde. |
| [**Windowsduplicatestring**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) | Erstellt eine Kopie der angegebenen Zeichenfolge. |
| [**Windowsgetstringlen**](/windows/win32/api/winstring/nf-winstring-windowsgetstringlen) | Ruft die Länge der angegebenen Zeichenfolge in Unicode-Zeichen ab. |
| [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) | Ruft den Unterstützungs Puffer für die angegebene Zeichenfolge ab. |
| [**Windowsinspectstring**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring) | Bietet eine Möglichkeit, für debuggger den Wert einer Windows-Runtime [**hstring**](hstring.md) in einem anderen Adressraum, Remote oder aus einem Dump anzuzeigen.  |
| [**WindowsInspectString2**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring2) | Bietet eine Möglichkeit, für debuggger den Wert einer Windows-Runtime [**hstring**](hstring.md) in einem anderen Adressraum, Remote oder aus einem Dump anzuzeigen.  |
| [**Windowsisstringempty**](/windows/win32/api/winstring/nf-winstring-windowsisstringempty) | Gibt an, ob die angegebene Zeichenfolge eine leere Zeichenfolge ist. |
| [**Windowshalzugecatestringbuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) | Ordnet einen änderbaren Zeichen Puffer zur Verwendung bei der [**hstring**](hstring.md) -Erstellung zu. |
| [**Windowspromotestringbuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) | Erstellt eine [**hstring**](hstring.md) aus dem angegebenen [**hstring- \_ Puffer**](hstring-buffer.md). |
| [**Windowsreplacestring**](/windows/win32/api/winstring/nf-winstring-windowsreplacestring) | Ersetzt alle Vorkommen eines Satzes von Zeichen in der angegebenen Zeichenfolge durch einen anderen Satz von Zeichen, um eine neue Zeichenfolge zu erstellen. |
| [**Windowsstringhasembeddednull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) | Gibt an, ob die angegebene Zeichenfolge eingebettete NULL-Zeichen enthält. |
| [**Windowssubstring**](/windows/win32/api/winstring/nf-winstring-windowssubstring) | Ruft eine Teil Zeichenfolge aus der angegebenen Zeichenfolge ab. Die Teil Zeichenfolge beginnt an der angegebenen Zeichenposition. |
| [**Windowssubstringwithspecifiedlength**](/windows/win32/api/winstring/nf-winstring-windowssubstringwithspecifiedlength) | Ruft eine Teil Zeichenfolge aus der angegebenen Zeichenfolge ab. Die Teilzeichenfolge beginnt an einer angegebenen Zeichenposition und hat eine angegebene Länge. |
| [**Windowstrimstringend**](/windows/win32/api/winstring/nf-winstring-windowstrimstringend) | Entfernt alle nachfolgenden Vorkommen eines angegebenen Zeichensatzes aus der Quell Zeichenfolge. |
| [**Windowstrimstringstart**](/windows/win32/api/winstring/nf-winstring-windowstrimstringstart) | Entfernt alle führenden Vorkommen eines angegebenen Zeichensatzes aus der Quell Zeichenfolge. |



 

 

 
