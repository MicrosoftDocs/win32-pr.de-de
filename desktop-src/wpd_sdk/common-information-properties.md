---
description: Windows Portable Geräte unterstützen die folgenden allgemeinen Informationseigenschaften.
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: Allgemeine Informationseigenschaften (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Common
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 41a8845a41714ed1a775d19e14f0996aad698aaf99de18da4eceb4df92688409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431103"
---
# <a name="common-information-properties"></a>Allgemeine Informationseigenschaften

Windows Portable Geräte unterstützen die folgenden allgemeinen Informationseigenschaften.



| Eigenschaft                                      | VarType        | Beschreibung                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| **\_WPD – ALLGEMEINE \_ \_ INFORMATIONSHINWEISE**           | **VT \_ LPWSTR** | Für Termine, Aufgaben und ähnliche Objekte enthält diese Eigenschaft alle Hinweise für das angegebene Objekt.     |
| **WPD \_ COMMON \_ INFORMATION \_ SUBJECT**         | **VT \_ LPWSTR** | Ein -Wert, der das Betrefffeld dieses Objekts angibt.                                                 |
| **WPD \_ COMMON \_ INFORMATION \_ BODY \_ TEXT**      | **VT \_ LPWSTR** | Diese Eigenschaft enthält den Textkörper eines Objekts im Klartext- oder HTML-Format.                          |
| **WPD \_ COMMON \_ INFORMATION \_ PRIORITY**        | **VT \_ UI4**    | Ein -Wert, der die Priorität dieses Objekts angibt. 0 gibt die höchste Priorität an.                    |
| **WPD \_ COMMON \_ INFORMATION \_ START \_ DATETIME** | **VT \_ DATE**   | Ein -Wert, der das Datum/die Uhrzeit des Starts eines Termins, einer Aufgabe oder eines ähnlichen Objekts angibt. |
| **WPD \_ COMMON \_ INFORMATION \_ END \_ DATETIME**   | **VT \_ DATE**   | Ein -Wert, der das Datum/die Uhrzeit angibt, zu der ein Termin, eine Aufgabe oder ein ähnliches Objekt beendet werden soll.   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und -Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




