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

Der Pfad zur zu verarbeitenden Ausnahme-INF.

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
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <dt>**COMP \_ FLAGS \_ FORCE**</dt> <dt>0x00000020</dt> </dl>                             | Überspringt die Versionsüberprüfung für Dateiersetzungen.<br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <dt>**COMP \_ FLAGS \_ MÜSSEN DEINSTALLIERT \_ WERDEN**</dt><dt></dt> </dl>        | Sichern Sie Dateien, die aktualisiert werden, damit sie von einer Deinstallation der Komponente verwendet werden.<br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <dt>**COMP \_ FLAGS \_ KEINE \_ ÜBERSCHREIBUNG**</dt><dt></dt> </dl>                 | Überspringt das Sichern von Dateien, wenn die Version der Ausnahmekomponente mit einer installierten Komponente identisch ist. Dieses Flag wird in einem Neuinstallationsszenario verwendet.<br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**COMP \_ FLAGS \_ NOUI-0x00000002**</dt> <dt></dt> </dl>                                | Unterdrückt alle Benutzeroberflächen.<br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**COMP \_ FLAGS \_ UPDATE \_ DLLCACHE**</dt><dt></dt> </dl>        | Erzwingt, dass das DLLCACHE-Verzeichnis aktualisiert wird, wenn eine Systemdatei aktualisiert wird.<br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**COMP \_ FLAGS \_ VERWENDEN \_ SVCPACK \_ CACHE**</dt><dt></dt> </dl> | Verwendet Dateien, die von einer Windows Service Pack-Installation zwischengespeichert werden, um die von ihnen gespeicherten Dateien zu verdringen.<br/>                                                                |



 

</dd> <dt>

*VerMajor* \[ in, optional\]
</dt> <dd>

Die Hauptversion der Ausnahmekomponente.

</dd> <dt>

*VerMinor* \[ in, optional\]
</dt> <dd>

Die Nebenversion der Exception-Komponente.

</dd> <dt>

*VerBuild* \[ in, optional\]
</dt> <dd>

Die Buildversion der Ausnahmekomponente.

</dd> <dt>

*VerQFE* \[ in, optional\]
</dt> <dd>

Die Hotfixrevision der Ausnahmekomponente.

</dd> <dt>

*Name* \[ in, optional\]
</dt> <dd>

Die beschreibende Zeichenfolge der Komponente, die im Dialogfeld Windows-Dateischutz angezeigt wird, wenn das Betriebssystem erkennt, dass eine Windows File Protection-Schutzdatei beschädigt, manipuliert oder beschädigt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen **HRESULT-Wert** zurück (S \_ OK oder ein Fehlercode). Ein Fehlercode kann mit dem Wert 0x20000100 überprüft werden, um zu bestimmen, ob der Fehler darauf zurück liegt, dass ein Neustart erforderlich ist.

## <a name="remarks"></a>Hinweise

Ausnahmepakete sind Windows, die außerhalb eines vollständigen Pakets Windows veröffentlicht werden und Betriebssystemdateien aktualisieren. Ausnahmepakete werden nur von Betriebssystemteams verfasst, denen die Autorisierung zum Aktualisieren Windows systemdateien erteilt wurde.

Verwenden Sie zum Installieren und Deinstallieren von Dateien, die nicht durch Windows File Protection geschützt sind, die Unter [Allgemeine Setupfunktionen dokumentierten Funktionen.](https://msdn.microsoft.com/library/ms794585.aspx) Zum Installieren von Gerätetreibern sollten Verkaufser Funktionen verwenden, die unter [Geräteinstallationsfunktionen](https://msdn.microsoft.com/library/ms792954.aspx) und [PnP-Konfigurations-Manager Functions dokumentiert sind.](https://msdn.microsoft.com/library/ms790838.aspx)

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



 

 
