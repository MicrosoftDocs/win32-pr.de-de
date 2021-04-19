---
description: Die Endpunkt-DLP-APIs (Data Loss Prevention, Verhinderung von Datenverlust) ermöglichen Es Anwendungen, das Betriebssystem vor und nach bestimmten Vorgängen zu benachrichtigen, z. B. beim Öffnen oder Speichern einer Datei.
title: Verhinderung von Endpunktdatenverlusten
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: 867e059e0accfc1208c96394c3065d69cf9f576c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495590"
---
# <a name="endpoint-data-loss-prevention"></a>Verhinderung von Endpunktdatenverlusten

Windows 10 implementiert Mechanismen, die dazu beitragen, Datenverluste für sensible Dateien zu verhindern. Die Endpunkt-DLP-APIs (Data Loss Prevention, Verhinderung von Datenverlust) ermöglichen Es Anwendungen, das Betriebssystem vor und nach bestimmten Vorgängen zu benachrichtigen, z. B. beim Öffnen oder Speichern einer Datei. Diese Benachrichtigungen dienen als "Hinweise", die es dem System ermöglichen, Datenverlustvorgänge zu optimieren.

## <a name="location-of-the-dlp-dll"></a>Speicherort der DLP-DLL

Da die Endpunkt-DLP-DLL nicht mit dem Windows SDK gebündelt ist, müssen Anwendungen die DLL zur Laufzeit manuell laden. Der Pfad zum SPEICHERORT DER DLL wird in der Registrierung gespeichert. In der folgenden Tabelle sind die Registrierungsschlüssel und -werte aufgeführt, in denen diese Informationen gespeichert werden. Diese Pfade werden als Konstanten in der unten angegebenen Codeauflistung endpointdlp.h definiert, um Entwicklern den Komfort zu bieten.

| Konstant | Wert | Beschreibung   |
|----------|-------|---------------|
| ENDPOINTDLP_DLL_NAME | "EndpointDlp.dll" | Der Name der Endpunkt-DLP-DLL, die die API bietet |
| ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY | "SOFTWARE \\ Microsoft \\ Windows Defender" | Windows Defender registrierungsschlüssel unter HKLM, in dem einige Endpunkt-DLP-Einstellungen gespeichert sind |
| ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY | Wert von ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY |  Der Registrierungspfad unter dem HKLM-Schlüssel, von dem EndpointDlp.dll Installationsspeicherort erhalten werden kann. |
| ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE | "InstallLocation" | Der Registrierungswert unter ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY, in dem der EndpointDlp.dll Installationsspeicherort gespeichert ist. |
| ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX | "x86" | Verketten Sie dieses Verzeichnis auf x64-Plattformen, um die x86-Version von EndpointDlp.dll |

## <a name="check-if-endpoint-dlp-is-enabled"></a>Überprüfen, ob Endpunkt-DLP aktiviert ist

Überprüfen Sie den folgenden Registrierungsschlüsselwert, um zu ermitteln, ob endpunkt-DLP auf dem System aktiviert ist. 

| Konstant | Wert | Beschreibung   |
|----------|-------|---------------|
| ENDPOINTDLP_ENABLED_FLAG_REGKEY |  \\"Features" | Der Pfad zum Flagschlüssel mit aktivierter Endpunkt-DLP unter (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY |
| ENDPOINTDLP_ENABLED_FLAG_REGVALUE | "SenseDlpEnabled" | Der Registrierungswert unter ENDPOINTDLP_ENABLED_FLAG_REGKEY, der den Registrierungsschlüssel des DLP-fähigen Flags enthält.

## <a name="endpoint-dlp-apis"></a>Endpunkt-DLP-APIs

In den folgenden Tabellen sind die APIs aufgeführt, die von der Endpunkt-DLP-DLL bereitgestellt werden.

### <a name="initialization-and-versioning"></a>Initialisierung und Versionierung

| API | Beschreibung |
|-----|-------------|
| [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md)                       | Benachrichtigt das System über die gewünschten Erzwingungsmodi für eine Reihe von DLP-Vorgängen (Endpoint Data Loss Prevention).                                  |
| [DlpGetEnforcementApiVersion](endpointdlp-dlpgetenforcementapiversion.md)                       | Ruft die Version der Endpunkt-DLP-API (Data Loss Prevention) auf dem aktuellen Gerät ab.                                  |


### <a name="document-operations"></a>Dokumentenvorgänge

| API | Beschreibung |
|-----|-------------|
| [DlpNotifyPreOpenDocument](endpointdlp-dlpnotifypreopendocument.md) | Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor der Öffnen-Vorgang initiiert wird. |
| [DlpNotifyPostOpenDocument](endpointdlp-dlpnotifypostopendocument.md) | Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem der Öffnen-Vorgang abgeschlossen wurde.  |
| [DlpNotifyCloseDocument](endpointdlp-dlpnotifyclosedocument.md)                       | Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor der Vorgang zum Schließen des Dokuments initiiert wird.                                  |
| [DlpNotifyPreOpenDocumentFile](endpointdlp-dlpnotifypreopendocumentfile.md)                         | Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor der Öffnen-Vorgang initiiert wird.  |
| [DlpNotifyPostOpenDocumentFile](endpointdlp-dlpnotifypostopendocumentfile.md)                       | Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem der Öffnen-Vorgang abgeschlossen wurde.                                  |
| [DlpNotifyCloseDocumentFile](endpointdlp-dlpnotifyclosedocumentfile.md)                       | Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor der Vorgang zum Schließen des Dokuments initiiert wird.                                  |

### <a name="save-as-operations"></a>Speichern als Vorgänge
| API | Beschreibung |
|-----|-------------|
| [DlpNotifyPreSaveAsDocument](endpointdlp-dlpnotifypresaveasdocument.md)                       | Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Save as-Vorgang initiiert wird.                                  |
| [DlpNotifyPostSaveAsDocument](endpointdlp-dlpnotifypostsaveasdocument.md)                       | Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem der Vorgang zum Speichern unter abgeschlossen wurde.                                  |


### <a name="drag-and-drop-operations"></a>Drag &amp; Drop-Vorgänge

| API | Beschreibung |
|-----|-------------|
| [DlpNotifyEnterDropTarget](endpointdlp-dlpnotifyenterdroptarget.md)                       | Stellt dem System Informationen zu einem Dokument zur Verfügung, wenn ein Abbruchziel eingegeben wird.                                  |
| [DlpNotifyLeaveDropTarget](endpointdlp-dlpnotifyleavedroptarget.md)                       | Stellt dem System Informationen zu einem Dokument bereit, wenn ein Ablageziel beendet wird.                                  |
| [DlpNotifyPreDragDrop](endpointdlp-dlpnotifypredragdrop.md)                         | Stellt dem System Informationen zu einem Dokument bereit, bevor ein Drag &amp; Drop-Vorgang initiiert wird.  |
| [DlpNotifyPostDragDrop](endpointdlp-dlpnotifypostdragdrop.md)                         | Stellt dem System Informationen zu einem Dokument bereit, nachdem ein Drag &amp; Drop-Vorgang abgeschlossen wurde.  |


### <a name="clipboard-operations"></a>Zwischenablagevorgänge

| API | Beschreibung |
|-----|-------------|
| [DlpNotifyPreCopyToClipboard](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | Stellt dem System Informationen zu einem Dokument bereit, bevor ein Kopiervorgang in die Zwischenablage initiiert wird.  |
| [DlpNotifyPostCopyToClipboard](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | Stellt dem System Informationen zu einem Dokument bereit, nachdem ein Kopiervorgang in die Zwischenablage abgeschlossen wurde.  |
| [DlpNotifyPrePasteFromClipboard](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | Stellt dem System Informationen zu einem Dokument bereit, bevor ein Einfügen aus der Zwischenablage initiiert wird.  |
| [DlpNotifyPostPasteFromClipboard](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | Stellt dem System Informationen zu einem Dokument bereit, nachdem ein Einfügevorgang aus der Zwischenablage abgeschlossen wurde.                                  |
| [DlpNotifyPostStashClipboard](endpointdlp-dlpnotifypoststashclipboard.md)                       | Stellt dem System Statusinformationen bereit, nachdem ein Stash-Zwischenablagevorgang abgeschlossen wurde.                                  |
| [DlpNotifyPreStashClipboard](endpointdlp-dlpnotifyprestashclipboard.md)                       | Benachrichtigt das System, bevor ein Stash-Zwischenablagevorgang initiiert wird.                                  |
| [DlpMustPasteFromSystemClipboard](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | Bestimmt, ob die App die Daten aus der Zwischenablage des Systems abrufen muss, anstatt sie aus dem internen Cache zu entfernen.                                  |

### <a name="print-operations"></a>Druckvorgänge

| API | Beschreibung |
|-----|-------------|
| [DlpNotifyPrePrint](endpointdlp-dlpnotifypreprint.md)                         | Stellt dem System Informationen zu einem Dokument zur Verfügung, bevor ein Druckvorgang initiiert wird.  |
| [DlpNotifyPostStartPrint](endpointdlp-dlpnotifypoststartprint.md)                       | Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem ein Druckvorgang gestartet wurde.                                  |
| [DlpNotifyPostPrint](endpointdlp-dlpnotifypostprint.md)                       | Stellt dem System Informationen zu einem Dokument zur Verfügung, nachdem ein Druckvorgang abgeschlossen wurde.                                  |

## <a name="endpoint-dlp-example-header"></a>Endpunkt-DLP-Beispielheader

Da der Endpunkt-DLP-Header nicht im Windows SDK enthalten ist, müssen Sie die Headerdatei selbst erstellen, um API-Signaturen für die Verwendung in Ihrer Implementierung zu erhalten. Der Einfachheit halber stellen wir Beispielcode zur Verfügung, den Sie kopieren und in Ihre Anwendung einfügen können. Zusätzlich zu Funktionsdeklarationen definiert diese Codeauflistung auch nützliche Konstanten wie Versionsinformationen und Registrierungsschlüsselpfade.

```cpp
//
// EndpointDlp DLL name containing the Endpoint DLP API
//

#define ENDPOINTDLP_DLL_NAME L"EndpointDlp.dll"

//
// Windows Defender registry key under HKLM where some Endpoint DLP settings are stored
//

#define ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"SOFTWARE\\Microsoft\\Windows Defender"

//
// EndpointDlp.dll install location can be obtained from the registry under the following HKLM key
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY

//
// EndpointDlp.dll install location is stored under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in the following registry value
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE L"InstallLocation"

//
// On x64 platforms, concatanate the following directory to obtain the x86 version of EndpointDlp.dll
//

#define ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX L"x86"

//
// Endpoint DLP enabled flag can be found under the following HKLM key
//

#define ENDPOINTDLP_ENABLED_FLAG_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"\\Features"

//
// Endpoint DLP enabled flag can be found under ENDPOINTDLP_ENABLED_REGKEY in the following registry value
//

#define ENDPOINTDLP_ENABLED_FLAG_REGVALUE L"SenseDlpEnabled"


#define DLP_DOCUMENT_INFO_V_1 0x1     

#define DLP_DOCUMENT_INFO_V_LATEST DLP_DOCUMENT_INFO_V_1


//
//  Enlightened app enforcement capablities.
//

typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, // No enforcement, DLP enforces operation.
    DlpAppEnforceLevelNotify,   // App send notifications on operation, DLP enforces operation.
    DlpAppEnforceLevelPrevent,  // Currently not supported (App allows or blocks operation, DLP enforces warning, eventing and UI). 
    DlpAppEnforceLevelFull,     // Currently not supported (App handles all enforcement (blocks operation, enforces warning, UI), DLP will only handle auditing.)
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;

typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
    
//
//  The stucture describes the enforcement level for each operation.
//
    
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;


/*
Function description:
     The application calls this functio to declares the enforcement level for each operation.

Parameters:
    _In_ DWORD Count - Number of operations. 
    _In_reads_opt_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL* OperationEnforcement - Array indicating operations
    supported by the application and enforcement level:
        DlpAppEnforceLevelNone - No enforcement, DLP enforces operation.
        DlpAppEnforceLevelNotify -  App send notifications on operation, DLP enforces operation.

Return:
    S_OK - Function completed successfully.
    E_INVALIDARG - Invalid parameters passed to function.
    E_OUTOFMEMORY - Memory allocation failed.
    E_XXX - Varius error codes.
*/       
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);


/*
Function description:
    Returns the version of the enforcement API.
    MajorVersion indicates a new interfaces/API.
    MinorVersion indicates changes to existing interfaces/API-s.
   
Parameters:
    None.

Return:
    S_OK - Function completed successfully
    E_XXX - Varius error codes.
*/
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);


typedef struct _DLP_DOCUMENT_INFO {

    //
    //  Information version. Always set it to DLP_DOCUMENT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Original path of the document.
    //  
    
    LPCWSTR PersistentFileName;

    //
    //  Path to the real backing file.
    //
    
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;

//
//  Post operation status information.
//
    
#define DLP_POSTOP_STATUS_V_1 0x1     
        
#define DLP_POSTOP_STATUS_V_LATEST DLP_POSTOP_STATUS_V_1;
    
       
typedef struct _DLP_POSTOP_STATUS {

    //
    //  Information version. Always set it to DLP_POSTOP_STATUS_V_LATEST
    //
    
    DWORD Version;

    //
    //  Set to TRUE if app's operation succeeded, FALSE otherwise. 
    //
    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS;    


#define DLP_PRINT_INFO_V_1 0x1     
    
#define DLP_PRINT_INFO_V_LATEST DLP_PRINT_INFO_V_1;

typedef struct _DLP_PRINT_INFO {

    //
    //  Information version. Always set it to DLP_PRINT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Destination printer.
    //
    
    LPCWSTR PrinterName;

    //
    //  Print job name.
    //
    
    LPCWSTR JobName;

    //
    //  Output file, if printing to file.
    //

    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;

    
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreStashClipboard();
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
    
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 


```


