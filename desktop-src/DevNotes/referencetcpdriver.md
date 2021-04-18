---
description: Ruft einen Verweis auf ein TCP V4-Treiber Objekt ab.
ms.assetid: 8f12fa58-1622-40d0-9a99-e7c8ede08b38
title: Referencetcpdriver-Funktion
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
ms.openlocfilehash: 4a9068739517cceedee72a675739b2d8b067b2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352119"
---
# <a name="referencetcpdriver-function"></a>Referencetcpdriver-Funktion

Ruft einen Verweis auf ein TCP V4-Treiber Objekt ab.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI ReferenceTcpDriver(
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

[**ReferenceTcpDriverV6**](referencetcpdriverv6.md)
</dt> </dl>

 

 




