---
title: FreeSoHAttributeValue-Funktion (NapUtil.h)
description: Gibt eine SoHAttributeValue-Datenstruktur frei.
ms.assetid: 21647ee6-2ea2-45fd-b1f2-fb1836196f94
keywords:
- FreeSoHAttributeValue-Funktion NAP
topic_type:
- apiref
api_name:
- FreeSoHAttributeValue
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 877a333c7eb43c3921c7727bcc15a958bdcd2565fabe4636a67868f3a27bf473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940404"
---
# <a name="freesohattributevalue-function"></a>FreeSoHAttributeValue-Funktion

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **FreeSoHAttributeValue-Funktion** gibt eine [**SoHAttributeValue-Datenstruktur**](sohattributevalue-union.md) frei.

## <a name="syntax"></a>Syntax


```C++
NAPAPI VOID WINAPI FreeSoHAttributeValue(
  _In_ SoHAttributeType  type,
  _In_ SoHAttributeValue *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*type* \[ In\]
</dt> <dd>

Ein [**SoHAttributeType-Wert,**](sohattributetype-enum.md) der den Typ des frei zu gebenden SoH-Attributwerts angibt.

</dd> <dt>

*value* \[ In\]
</dt> <dd>

Ein Zeiger auf den frei zu [**gebenden SoHAttributeValue.**](sohattributevalue-union.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Alle vom NAP-System unterstützten COM-Schnittstellen verwenden standardmäßige COM-Speicherverwaltungsregeln und die COM-Speicherzuweisungen (**CoTaskMemAlloc** und **CoTaskMemFree**):

-   **In** werden Parameter vom Aufrufer zugeordnet und frei.
-   **Out-Parameter** werden vom Aufrufer zugeordnet und vom Aufrufer mithilfe von **CoTaskMem frei.**
-   **Ein-/Aus-Parameter** werden vom Aufrufer zugeordnet, vom Aufrufer frei und neu zugeordnet und schließlich vom Aufrufer mithilfe von **CoTaskMem frei.**

Alle NAP-Funktionen zum Freien von Arbeitsspeicher geben auch alle eingebetteten Zeiger frei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 





