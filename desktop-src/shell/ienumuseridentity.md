---
description: Ienumumuseridentity wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: df4b6235-e66a-4187-b1f9-33c042cae2f2
title: Ienumumuseridentity-Schnittstelle (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 48abf182942f90ecd477a241be3bf45323bdbdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979504"
---
# <a name="ienumuseridentity-interface"></a>Ienumumuseridentity-Schnittstelle

\[**Ienumumuseridentity** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

Stellt eine Enumeration aller Benutzer Identitäten bereit, die auf dem System vorhanden sind.

## <a name="members"></a>Member

Die **ienumumuseridentity** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ienumuseridentity** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ienumumuseridentity** -Schnittstelle verfügt über diese Methoden.



| Methode                                         | BESCHREIBUNG                                                                                                                  |
|:-----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**Klon**](ienumuseridentity-clone.md)       | Veraltet. Ruft eine Kopie der aktuellen Enumeration ab.<br/>                                                               |
| [**GetCount**](ienumuseridentity-getcount.md) | Veraltet. Ruft die Anzahl der Benutzer Identitäten ab, die sich zurzeit im System befinden.<br/>                                            |
| [**Weiter**](ienumuseridentity-next.md)         | Veraltet. Ruft ein Array von Benutzer Identitäts Schnittstellen aus der-Enumeration ab.<br/>                                  |
| [**Festlegen**](ienumuseridentity-reset.md)       | Veraltet. Setzt die interne Anzahl der abgerufenen Schnittstellen in der-Enumeration zurück.<br/>                                 |
| [**Überspringen**](ienumuseridentity-skip.md)         | Veraltet. Überspringt eine angegebene Anzahl von Benutzer Identitäts Schnittstellen in der-Enumeration. Wird beim Abrufen von Schnittstellen verwendet.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Zum Abrufen von Informationen zu Benutzer Identitäten, die auf dem System vorhanden sind, können Sie diese Schnittstelle verwenden. Über eine [**iuseridentitymanager**](iuseridentitymanager.md) -Schnittstelle können Sie [**iuseridentitymanager:: tumidentities**](iuseridentitymanager-enumidentities.md) aufrufen, um diese Schnittstelle abzurufen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                  |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Iuseridentitymanager**](iuseridentitymanager.md)
</dt> </dl>

 

 
