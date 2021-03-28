---
description: Iuseridentitymanager::-Eigenschaften werden nicht unterstützt und können in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: 8111fbcd-dc4d-45cb-83e0-3c2cd7c4df27
title: 'Iuseridentitymanager:: sumidentities-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.EnumIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3109867651b69e311639d8b2e70e5f02e33a3dc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127833"
---
# <a name="iuseridentitymanagerenumidentities-method"></a>Iuseridentitymanager:: sumidentities-Methode

\[**Iuseridentitymanager::-Eigenschaften** werden nicht unterstützt und können in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

Ruft ein [**ienumuseridentity**](ienumuseridentity.md) -Objekt ab, das verwendet werden kann, um die Benutzer Identitäten aufzulisten, die auf dem System vorhanden sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumIdentities(
  [out] IEnumUserIdentity **ppEnumUser
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *ppumuser* \[ " vorgenommen\]
</dt> <dd>

Typ: **[ **iumumuseridentity**](ienumuseridentity.md)\*\***

Die Adresse des Zeigers auf das neue identitätsenumerationsobjekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Das Ergebnis des Abruf Vorgangs. Bei erfolgreicher Ausführung wird S OK zurückgegeben \_ . Wenn das Enumerationsobjekt nicht erstellt werden konnte, wird E \_ outo-Memory zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode ist nützlich für die iterierung der Liste der Identitäten im System. Um eine einzelne Identität über das Cookie abzurufen, ohne auf die Liste zuzugreifen, rufen Sie [**iuseridentitymanager:: getidentitybycookie**](iuseridentitymanager-getidentitybycookie.md)auf.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Iuseridentitymanager**](iuseridentitymanager.md)
</dt> <dt>

[**Iumumuseridentity**](ienumuseridentity.md)
</dt> <dt>

[**Iuseridentitymanager:: getidentitybycookie**](iuseridentitymanager-getidentitybycookie.md)
</dt> </dl>

 

 




