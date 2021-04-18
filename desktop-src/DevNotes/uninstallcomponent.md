---
description: Entfernt ein Ausnahme Paket.
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: Uninstallcomponent-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UninstallComponent
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: a541f51b030c9be7a26d573794e4df3a7cfc6f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365899"
---
# <a name="uninstallcomponent-function"></a>Uninstallcomponent-Funktion

Entfernt ein Ausnahme Paket.

## <a name="syntax"></a>Syntax


```C++
void UninstallComponent(
  _In_opt_ const GUID  *CompGuid,
  _In_           DWORD Flags,
  _In_opt_       INT   VerMajor,
  _In_opt_       INT   VerMinor,
  _In_opt_       INT   VerBuild,
  _In_opt_       INT   VerQFE
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Compguid* \[ in, optional\]
</dt> <dd>

Der GUID der Ausnahme Komponente, die deinstalliert wird.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Die Flags, die zum Steuern des Installations Verhaltens verwendet werden. Dieser Parameter kann eine Kombination der folgenden Werte sein.



| Wert                                                                                                                                                                                                         | Bedeutung                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**Comp \_ Flags \_ NoUI**</dt> </dl>                                          | Unterdrückt die gesamte Benutzeroberfläche.<br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**Comp- \_ Flags \_ Aktualisieren von \_ Dllcache**</dt> </dl>        | Erzwingt die Aktualisierung des Dllcache-Verzeichnisses, wenn eine Systemdatei aktualisiert wird.<br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**Comp- \_ Flags \_ verwenden den \_ Svcpack- \_ Cache.**</dt> </dl> | Verwendet Dateien, die von einer Windows-Service Pack Installation zwischengespeichert werden, um die gesicherten Dateien abzuersetzen.<br/> |



 

</dd> <dt>

*VerMajor* \[ in, optional\]
</dt> <dd>

Die Hauptversion der Ausnahme Komponente, die deinstalliert werden soll.

</dd> <dt>

*VerMinor* \[ in, optional\]
</dt> <dd>

Die neben Version der Ausnahme Komponente, die deinstalliert werden soll.

</dd> <dt>

*Verbuild* \[ in, optional\]
</dt> <dd>

Die Buildversion der Ausnahme Komponente, die deinstalliert werden soll.

</dd> <dt>

*Verqfe* \[ in, optional\]
</dt> <dd>

Die hotfixrevision der Ausnahme Komponente, die deinstalliert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Ausnahme Pakete sind Windows-Systemdateien, die außerhalb eines vollständigen Paket-Windows-Release freigegeben werden und die Betriebssystemdateien aktualisieren. Ausnahme Pakete werden nur von Betriebssystem Teams erstellt, denen eine Autorisierung zum Aktualisieren von Windows-Systemdateien erteilt wurde.

Verwenden Sie zum Installieren und Deinstallieren von Dateien, die nicht durch den Windows-Datei Schutz geschützt sind, die unter [Allgemeine Setup Funktionen](https://msdn.microsoft.com/library/ms794585.aspx)dokumentierten Funktionen. Für die Installation von Gerätetreibern sollten vender Funktionen verwenden, [](https://msdn.microsoft.com/library/ms792954.aspx) die in geräteregistrierungs-und [PNP-Configuration Manager Funktionen](https://msdn.microsoft.com/library/ms790838.aspx)dokumentiert sind.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>


</dt> <dt>

[**Installcomponentw**](installcomponentw.md)
</dt> </dl>

 

 
