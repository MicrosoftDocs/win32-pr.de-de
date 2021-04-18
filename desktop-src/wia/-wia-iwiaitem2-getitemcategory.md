---
description: Ruft die Kategorieinformationen eines Elements ab.
ms.assetid: 4d6f7a6a-280d-4b36-8e1d-8d9fcaa8a1de
title: 'IWiaItem2:: getitemcategory-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemCategory
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: fdf650e8b540fcb9dc58f93f34771462fbc0a5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344455"
---
# <a name="iwiaitem2getitemcategory-method"></a>IWiaItem2:: getitemcategory-Methode

Ruft die Kategorieinformationen eines Elements ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetItemCategory(
  [out] GUID *pItemCategoryGUID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pitemcategoryguid* \[ vorgenommen\]
</dt> <dd>

Geben Sie Folgendes ein: **GUID \** _

Empfängt einen Zeiger auf die GUID, die die Kategorie des Elements identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Jedes [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt in der hierarchischen Struktur von Objekten, das einem Windows-Abbild Abruf (WIA) 2,0-Hardware Gerät zugeordnet ist, verfügt über eine bestimmte Kategorie. Diese Methode ermöglicht es Anwendungen, die Kategorie beliebiger Elemente in einer hierarchischen Struktur von Element Objekten in einem Gerät zu identifizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




