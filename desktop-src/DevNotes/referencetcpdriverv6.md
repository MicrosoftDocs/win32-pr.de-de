---
description: Ruft einen Verweis auf ein TCP-V6-Treiber Objekt ab.
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
ms.openlocfilehash: d0a3f56ea59eb753dc7a49d6f6b1d0c48be8abca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365776"
---
# <a name="referencetcpdriverv6-function"></a>ReferenceTcpDriverV6-Funktion

Ruft einen Verweis auf ein TCP-V6-Treiber Objekt ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI ReferenceTcpDriverV6(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppdriverobject* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine **Treiber \_ Objekt** Struktur. Weitere Informationen finden Sie in der Dokumentation für das WDK.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben. Wenn ein Fehler auftritt, wird der entsprechende Statuscode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Funktion kann nur aus dem Kernel Modus aufgerufen werden. Der Aufrufer muss den Verweis Zähler verringern, indem er die **obdereferenceobject** -Funktion aufruft, wenn er mit dem-Objekt abgeschlossen ist.

Diese Funktion ist in drvref. lib implementiert, das zum Download verfügbar ist. Siehe [Referenz-API-Bibliothek für Windows-Netzwerktreiber](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Drvref. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Referencetcpdriver**](referencetcpdriver.md)
</dt> </dl>

 

 




