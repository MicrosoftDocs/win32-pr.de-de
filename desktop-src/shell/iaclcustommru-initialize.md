---
description: Lädt eine Liste von Zeichen folgen in die Liste der zuletzt verwendeten (MRU-) Einträge aus der Registrierung.
title: 'Iaclcustommru:: Initialize-Methode'
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
ms.openlocfilehash: 768df625cb66c888ddccc85f72de5b8676c20b10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994631"
---
# <a name="iaclcustommruinitialize-method"></a>Iaclcustommru:: Initialize-Methode

Lädt eine Liste von Zeichen folgen in die Liste der zuletzt verwendeten (MRU-) Einträge aus der Registrierung.

## <a name="syntax"></a>Syntax


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszmruregkey* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf einen Puffer, der den Registrierungsschlüssel enthält, der die Zeichen folgen für die MRU-Liste enthält.

</dd> <dt>

*dwMax* \[ in\]
</dt> <dd>

Typ: **DWORD**

Die maximale Anzahl von Einträgen, die von *pwszmruregkey* entnommen werden können.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



 

 




