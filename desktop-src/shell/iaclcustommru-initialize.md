---
description: Lädt eine Liste von Zeichenfolgen in die Liste der zuletzt verwendeten (MRU) aus der Registrierung.
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
ms.openlocfilehash: 715c6991021070dd132942de0bb18c8b77684860
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841231"
---
# <a name="iaclcustommruinitialize-method"></a>IACLCustomMRU::Initialize-Methode

Lädt eine Liste von Zeichenfolgen in die Liste der zuletzt verwendeten (MRU) aus der Registrierung.

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

Ein Zeiger auf einen Puffer, der den Registrierungsschlüssel mit den Zeichenfolgen für die MRU-Liste enthält.

</dd> <dt>

*dwMax* \[ In\]
</dt> <dd>

Typ: **DWORD**

Die maximale Anzahl von Einträgen, die aus *pwszMRURegKey* entnommen werden können.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/> |



 

 




