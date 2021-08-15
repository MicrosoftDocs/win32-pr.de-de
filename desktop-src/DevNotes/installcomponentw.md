---
description: Installiert ein Ausnahmepaket.
ms.assetid: c4c3c01c-9aaf-42cd-a690-13e2113b15b3
title: InstallComponentW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallComponentW
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: 9deaa460ec58ad0aa07af38aa03f53971068b4a6a1d43131e5473a7e4def908c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955919"
---
# <a name="installcomponentw-function"></a>InstallComponentW-Funktion

Installiert ein Ausnahmepaket.

## <a name="syntax"></a>Syntax


```C++
void InstallComponentW(
  _In_           LPCWSTR InfPath,
  _In_opt_ const GUID    *CompGuid,
  _In_           DWORD   Flags,
  _In_opt_       INT     VerMajor,
  _In_opt_       INT     VerMinor,
  _In_opt_       INT     VerBuild,
  _In_opt_       INT     VerQFE,
  _In_opt_       LPCWSTR Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*InfPath* \[ In\]
</dt> <dd>

Der Pfad zur ausnahme-INF, die verarbeitet werden soll.

</dd> <dt>

*CompGuid* \[ in, optional\]
</dt> <dd>

Die GUID der Ausnahmekomponente, die installiert wird.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Die Flags, die zum Steuern des Installationsverhaltens verwendet werden. Dieser Parameter kann eine Kombination der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <dt>**COMP \_ FLAGS \_ FORCE**</dt> <dt>0x00000020</dt> </dl>                             | Überspringt die Versionsprüfung für Dateiersetzungen.<br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <dt>**COMP \_ FLAGS \_ MÜSSEN \_ DEINSTALLIERT WERDEN**</dt><dt></dt> </dl>        | Sichern Sie Dateien, die aktualisiert werden, damit sie von einer Deinstallation der Komponente verwendet werden.<br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <dt>**COMP \_ FLAGS \_ OHNE \_ ÜBERSCHREIBEN**</dt><dt></dt> </dl>                 | Überspringt das Sichern von Dateien, wenn die Version der Ausnahmekomponente mit der einer installierten Komponente identisch ist. Dieses Flag wird in einem Neuinstallationsszenario verwendet.<br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**COMP \_ \_FLAGS NOUI**</dt> <dt>0x00000002</dt> </dl>                                | Unterdrückt die gesamte Benutzeroberfläche.<br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**COMP \_ FLAGS \_ UPDATE \_ DLLCACHE**</dt><dt></dt> </dl>        | Erzwingt, dass das DLLCACHE-Verzeichnis aktualisiert wird, wenn eine Systemdatei aktualisiert wird.<br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**COMP \_ FLAGS \_ VERWENDEN \_ SVCPACK \_ CACHE**</dt><dt></dt> </dl> | Verwendet Dateien, die von einer Windows Service Pack-Installation zwischengespeichert werden, um gesicherte Dateien zu ersetzen.<br/>                                                                |



 

</dd> <dt>

*VerMajor* \[ in, optional\]
</dt> <dd>

Die Hauptversion der Exception-Komponente.

</dd> <dt>

*VerMinor* \[ in, optional\]
</dt> <dd>

Die Nebenversion der Ausnahmekomponente.

</dd> <dt>

*VerBuild* \[ in, optional\]
</dt> <dd>

Die Buildversion der Exception-Komponente.

</dd> <dt>

*Ver SILKE* \[ in, optional\]
</dt> <dd>

Die Hotfixrevision der Ausnahmekomponente.

</dd> <dt>

*Name* \[ in, optional\]
</dt> <dd>

Die beschreibende Zeichenfolge der Komponente, die im Dialogfeld Windows Dateischutz angezeigt wird, wenn das Betriebssystem erkennt, dass eine Windows Dateischutzdatei beschädigt, manipuliert oder beschädigt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen **HRESULT-Wert** (S \_ OK oder einen Fehlercode) zurück. Ein Fehlercode kann anhand des Werts 0x20000100 überprüft werden, um zu ermitteln, ob der Fehler darauf zurückzuführen ist, dass ein Neustart erforderlich ist.

## <a name="remarks"></a>Hinweise

Ausnahmepakete sind Windows Systemdateien, die außerhalb eines vollständigen Pakets Windows Release veröffentlicht werden und Betriebssystemdateien aktualisieren. Ausnahmepakete werden nur von Betriebssystemteams erstellt, denen die Autorisierung zum Aktualisieren Windows Systemdateien erteilt wurde.

Verwenden Sie zum Installieren und Deinstallieren von Dateien, die nicht durch Windows Dateischutz geschützt sind, die in [Allgemeine Setupfunktionen dokumentierten](https://msdn.microsoft.com/library/ms794585.aspx)Funktionen. Zum Installieren von Gerätetreibern sollten Automaten Funktionen verwenden, die in [Geräteinstallationsfunktionen](https://msdn.microsoft.com/library/ms792954.aspx) und [PnP Konfigurations-Manager Functions](https://msdn.microsoft.com/library/ms790838.aspx)dokumentiert sind.

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



 

 
