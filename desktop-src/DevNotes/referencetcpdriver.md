---
description: Erhält einen Verweis auf ein TCP v4-Treiberobjekt.
ms.assetid: 8f12fa58-1622-40d0-9a99-e7c8ede08b38
title: ReferenceTcpDriver-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriver
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: 36329ecb695c6fcc011f7e1fe4f44a149fbeac48b0125c34330b9bde51342f5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690840"
---
# <a name="referencetcpdriver-function"></a>ReferenceTcpDriver-Funktion

Erhält einen Verweis auf ein TCP v4-Treiberobjekt.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI ReferenceTcpDriver(
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

[**ReferenceTcpDriverV6**](referencetcpdriverv6.md)
</dt> </dl>

 

 




