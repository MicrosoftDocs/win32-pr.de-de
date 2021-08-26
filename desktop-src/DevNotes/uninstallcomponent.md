---
description: Entfernt ein Ausnahmepaket.
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: UninstallComponent-Funktion
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
ms.openlocfilehash: d6b4ce8e447bc884d1b3ee64505d230b2e069ce6cda1630b027b8a48da68beda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001110"
---
# <a name="uninstallcomponent-function"></a>UninstallComponent-Funktion

Entfernt ein Ausnahmepaket.

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

*CompGuid* \[ in, optional\]
</dt> <dd>

Die GUID der Ausnahmekomponente, die deinstalliert wird.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Die Flags, die zum Steuern des Installationsverhaltens verwendet werden. Dieser Parameter kann eine Kombination der folgenden Werte sein.



| Wert                                                                                                                                                                                                         | Bedeutung                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**COMP \_ FLAGS \_ NOUI**</dt> </dl>                                          | Unterdrückt alle Benutzeroberflächen.<br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**COMP \_ FLAGS \_ UPDATE \_ DLLCACHE**</dt> </dl>        | Erzwingt, dass das DLLCACHE-Verzeichnis aktualisiert wird, wenn eine Systemdatei aktualisiert wird.<br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**\_COMP-FLAGS \_ VERWENDEN \_ SVCPACK \_ CACHE**</dt> </dl> | Verwendet Dateien, die von einer Windows Service Pack-Installation zwischengespeichert werden, um die von ihnen gespeicherten Dateien zu verdringen.<br/> |



 

</dd> <dt>

*VerMajor* \[ in, optional\]
</dt> <dd>

Die Hauptversion der zu deinstallierenden Ausnahmekomponente.

</dd> <dt>

*VerMinor* \[ in, optional\]
</dt> <dd>

Die Nebenversion der Ausnahmekomponente, die deinstalliert werden soll.

</dd> <dt>

*VerBuild* \[ in, optional\]
</dt> <dd>

Die Buildversion der zu deinstallierenden Ausnahmekomponente.

</dd> <dt>

*VerQFE* \[ in, optional\]
</dt> <dd>

Die Hotfixrevision der zu deinstallierenden Ausnahmekomponente.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Ausnahmepakete sind Windows, die außerhalb eines vollständigen Pakets Windows veröffentlicht werden und Betriebssystemdateien aktualisieren. Ausnahmepakete werden nur von Betriebssystemteams verfasst, denen die Autorisierung zum Aktualisieren Windows systemdateien erteilt wurde.

Verwenden Sie zum Installieren und Deinstallieren von Dateien, die nicht durch Windows File Protection geschützt sind, die Unter [Allgemeine Setupfunktionen dokumentierten Funktionen.](https://msdn.microsoft.com/library/ms794585.aspx) Zum Installieren von Gerätetreibern sollten Verkaufser Funktionen verwenden, die unter [Geräteinstallationsfunktionen](https://msdn.microsoft.com/library/ms792954.aspx) und [PnP-Konfigurations-Manager Functions dokumentiert sind.](https://msdn.microsoft.com/library/ms790838.aspx)

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>


</dt> <dt>

[**InstallComponentW**](installcomponentw.md)
</dt> </dl>

 

 
