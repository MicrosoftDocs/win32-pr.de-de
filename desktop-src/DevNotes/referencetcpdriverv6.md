---
description: Erhält einen Verweis auf ein TCP v6-Treiberobjekt.
ms.assetid: 9f57ea0b-0ab4-4ef9-9bf1-1f41f72dfbe9
title: ReferenceTcpDriverV6-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriverV6
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: 7c8fc1a24b812608db74fa16b8dafc323fe48442d61d7d7b35c0d371c0828ad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571770"
---
# <a name="referencetcpdriverv6-function"></a>ReferenceTcpDriverV6-Funktion

Erhält einen Verweis auf ein TCP v6-Treiberobjekt.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI ReferenceTcpDriverV6(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDriverObject* \[ out\]
</dt> <dd>

Ein Zeiger auf eine **DRIVER \_ OBJECT-Struktur.** Weitere Informationen finden Sie in der Dokumentation zum WDK.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, wird **STATUS \_ SUCCESS zurückgegeben.** Wenn ein Fehler auftritt, wird der entsprechende Statuscode zurückgeben.

## <a name="remarks"></a>Hinweise

Diese Funktion kann nur im Kernelmodus aufgerufen werden. Der Aufrufer muss die Verweisanzahl durch Aufrufen der **ObDereferenceObject-Funktion** dekrementieren, wenn er mit dem -Objekt fertig ist.

Diese Funktion wird in "Dridof.lib" implementiert, die zum Download verfügbar ist. Weitere Informationen [finden Windows Referenz zur Netzwerktreiber-API-Bibliothek.](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Drrankf.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ReferenceTcpDriver**](referencetcpdriver.md)
</dt> </dl>

 

 




