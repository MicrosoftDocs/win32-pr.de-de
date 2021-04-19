---
title: Iwmdrmlicencbackuprestorestatus-Methode (wmdrmsdk. h)
description: Mit der GetStatus-Methode werden detaillierte Statusinformationen zu einer Lizenz Sicherung oder einem Wiederherstellungs Vorgang abgerufen.
ms.assetid: 1a695baf-0971-4dbf-90fa-1b10178a3348
keywords:
- GetStatus-Methode Windows Media-Format
- GetStatus-Methode Windows Media-Format, iwmdrmlicenabbackuprestorestatus-Schnittstelle
- Iwmdrmlicencbackuprestorestatus-Schnittstelle Windows Media-Format, GetStatus-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus.GetStatus
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3373e71bcae9dc1054e97e8b758ac72389b9a712
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367788"
---
# <a name="iwmdrmlicensebackuprestorestatusgetstatus-method"></a>Iwmdrmlicencbackuprestorestatus:: GetStatus-Methode

Mit der **GetStatus** -Methode werden detaillierte Statusinformationen zu einer Lizenz Sicherung oder einem Wiederherstellungs Vorgang abgerufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStatus(
  [out] WM_BACKUP_RESTORE_STATUS *pStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstatus* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine [**Status Struktur der WM- \_ Sicherungs \_ Wiederherstellung \_**](wm-backup-restore-status.md) , die die Statusinformationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicentbackuprestorestatus-Schnittstelle**](iwmdrmlicensebackuprestorestatus.md)
</dt> </dl>

 

 





