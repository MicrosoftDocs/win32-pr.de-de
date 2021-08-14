---
description: Fügt der Liste der zuletzt verwendeten (MRU) einen Eintrag hinzu.
title: IACLCustomMRU::AddMRUString-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.AddMRUString
api_type:
- COM
api_location: ''
ms.assetid: d8fb8fa5-452b-45fd-b015-d9bf3d0c642e
ms.openlocfilehash: e5acd71a56ef0dd569315ee924313b10e27e6a4ba7ca75d1dbfa0d1e50932cdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223594"
---
# <a name="iaclcustommruaddmrustring-method"></a>IACLCustomMRU::AddMRUString-Methode

Fügt der Liste der zuletzt verwendeten (MRU) einen Eintrag hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszEntry* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf einen Puffer, der den neuen Eintrag enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



 

 




