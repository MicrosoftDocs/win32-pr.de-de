---
description: Eine Anforderung zum Aktualisieren des Anfangszustands eines Objekts; z. B. eine Textur oder ein Shader.
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
ms.openlocfilehash: 1fddd375b72681b87ad9abf9abe679ece1725d6a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624636"
---
# <a name="span-idvspixengineiupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptrspaniupdateobjectupdateobject-method"></a><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>IUpdateObject::UpdateObject-Methode

Eine Anforderung zum Aktualisieren des Anfangszustands eines Objekts; z. B. eine Textur oder ein Shader.

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

*count1 \_ buffer*   
Die Updatenutzlast.

*pCallback*   
Die Adresse einer Funktion, die verwendet wird, um den Host darüber zu benachrichtigen, dass das Objekt aktualisiert wurde.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IUpdateObject**](/windows/desktop/direct3dtools/iupdateobject)

 

 
