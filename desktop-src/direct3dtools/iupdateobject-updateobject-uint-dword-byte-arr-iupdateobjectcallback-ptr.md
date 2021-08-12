---
description: Eine Anforderung zum Aktualisieren des Anfangszustands eines Objekts. z. B. eine Textur oder ein Shader.
MS-HAID: vspixengine.IUpdateObject\_UpdateObject\_UINT\_DWORD\_BYTE\_arr\_IUpdateObjectCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IUpdateObject::UpdateObject-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 824AB599-7377-4F77-8FC8-41E17ED57A79
api_name:
- IUpdateObject.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b48e206d09c784ac2f2df31eeab0d65cac04f740a66874fe9e436f96b8349143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282276"
---
# <a name="span-idvspixengineiupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptrspaniupdateobjectupdateobject-method"></a><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>IUpdateObject::UpdateObject-Methode

Eine Anforderung zum Aktualisieren des Anfangszustands eines Objekts. z. B. eine Textur oder ein Shader.

## <a name="syntax"></a>Syntax


```C++
HRESULT UpdateObject(
   UINT                    objectAddress,
   DWORD                   size,
   BYTE []                 count1_buffer,
   IUpdateObjectCallback * pCallback
);
```

## <a name="parameters"></a>Parameter

*objectAddress*   
Die ID des zu aktualisierenden Objekts.

*Größe*   
Die Größe der Updatenutzlast in Bytes.

*\_count1-Puffer*   
Die Updatenutzlast.

*pCallback*   
Die Adresse einer Funktion, mit der der Host benachrichtigt wird, dass das Objekt aktualisiert wurde.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IUpdateObject**](/windows/desktop/direct3dtools/iupdateobject)

 

 
