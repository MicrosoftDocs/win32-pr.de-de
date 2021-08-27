---
description: Lädt eine Liste von Zeichenfolgen in die Liste der zuletzt verwendeten Zeichenfolgen (MRU) aus der Registrierung.
title: IACLCustomMRU::Initialize-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.Initialize
api_type:
- COM
api_location: ''
ms.assetid: 358921b0-46c4-4428-b0b5-57a44fc3247b
ms.openlocfilehash: 0e0cad5f144a4ce97c648463cfdf31bf1c2ee7da0fb89b5508ce9386dba0f14f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111760"
---
# <a name="iaclcustommruinitialize-method"></a>IACLCustomMRU::Initialize-Methode

Lädt eine Liste von Zeichenfolgen in die Liste der zuletzt verwendeten Zeichenfolgen (MRU) aus der Registrierung.

## <a name="syntax"></a>Syntax


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszMRURegKey* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf einen Puffer, der den Registrierungsschlüssel enthält, der die Zeichenfolgen für die MRU-Liste enthält.

</dd> <dt>

*dwMax* \[ In\]
</dt> <dd>

Typ: **DWORD**

Die maximale Anzahl von Einträgen, die von *pwszMRURegKey übernommen werden können.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



 

 




