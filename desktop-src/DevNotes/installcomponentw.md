---
description: Installiert ein Ausnahme Paket.
ms.assetid: c4c3c01c-9aaf-42cd-a690-13e2113b15b3
title: Installcomponentw-Funktion
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
ms.openlocfilehash: 4d262322be6084429f03d5725f61c0e0f7140871
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373883"
---
# <a name="installcomponentw-function"></a>Installcomponentw-Funktion

Installiert ein Ausnahme Paket.

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

*INFPath* \[ in\]
</dt> <dd>

Der Pfad zur INF-Ausnahme, die verarbeitet werden soll.

</dd> <dt>

*Compguid* \[ in, optional\]
</dt> <dd>

Der GUID der zu installierenden Ausnahme Komponente.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Die Flags, die zum Steuern des Installations Verhaltens verwendet werden. Dieser Parameter kann eine Kombination der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                               | Bedeutung                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <dt>**Comp \_ Flags \_ erzwingen**</dt> <dt>0x00000020</dt> </dl>                             | Überspringt die Versions Überprüfung bei Datei Ersetzungen.<br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <dt>**Comp \_ Flags \_ müssen \_ deinstalliert**</dt> werden <dt></dt> </dl>        | Dient zum Sichern von Dateien, die zur Verwendung durch eine Deinstallation der Komponente aktualisiert werden.<br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <dt>**Comp \_ Flags \_ nicht über \_ Schreiben**</dt><dt></dt> </dl>                 | Überspringt das Sichern von Dateien, wenn die Ausnahme Komponenten Version mit der installierten Komponente identisch ist. Dieses Flag wird in einem Neuinstallations Szenario verwendet.<br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**Comp \_ Flags \_ NoUI**</dt> <dt>0x00000002</dt> </dl>                                | Unterdrückt die gesamte Benutzeroberfläche.<br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**Comp \_ Flags \_ Aktualisieren von \_ Dllcache**</dt><dt></dt> </dl>        | Erzwingt die Aktualisierung des Dllcache-Verzeichnisses, wenn eine Systemdatei aktualisiert wird.<br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**Comp \_ Flags \_ verwenden den \_ Svcpack- \_ Cache**</dt> . <dt></dt> </dl> | Verwendet Dateien, die von einer Windows-Service Pack Installation zwischengespeichert werden, um die gesicherten Dateien abzuersetzen.<br/>                                                                |



 

</dd> <dt>

*VerMajor* \[ in, optional\]
</dt> <dd>

Die Hauptversion der Ausnahme Komponente.

</dd> <dt>

*VerMinor* \[ in, optional\]
</dt> <dd>

Die neben Version der Ausnahme Komponente.

</dd> <dt>

*Verbuild* \[ in, optional\]
</dt> <dd>

Die Buildversion der Ausnahme Komponente.

</dd> <dt>

*Verqfe* \[ in, optional\]
</dt> <dd>

Die hotfixrevision der Ausnahme Komponente.

</dd> <dt>

*Name* \[ in, optional\]
</dt> <dd>

Die beschreibende Zeichenfolge der Komponente, die im Dialogfeld "Windows-Datei Schutz" angezeigt wird, wenn das Betriebssystem erkennt, dass eine Schutz Datei für den Windows-Datei Schutz beschädigt, manipuliert oder beschädigt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen **HRESULT** -Wert (S \_ OK oder einen Fehlercode) zurück. Ein Fehlercode kann mit dem Wert 0x20000100 verglichen werden, um zu bestimmen, ob der Fehler darauf liegt, dass ein Neustart erforderlich ist.

## <a name="remarks"></a>Bemerkungen

Ausnahme Pakete sind Windows-Systemdateien, die außerhalb eines vollständigen Paket-Windows-Release freigegeben werden und die Betriebssystemdateien aktualisieren. Ausnahme Pakete werden nur von Betriebssystem Teams erstellt, denen eine Autorisierung zum Aktualisieren von Windows-Systemdateien erteilt wurde.

Verwenden Sie zum Installieren und Deinstallieren von Dateien, die nicht durch den Windows-Datei Schutz geschützt sind, die unter [Allgemeine Setup Funktionen](https://msdn.microsoft.com/library/ms794585.aspx)dokumentierten Funktionen. Für die Installation von Gerätetreibern sollten vender Funktionen verwenden, [](https://msdn.microsoft.com/library/ms792954.aspx) die in geräteregistrierungs-und [PNP-Configuration Manager Funktionen](https://msdn.microsoft.com/library/ms790838.aspx)dokumentiert sind.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



 

 
