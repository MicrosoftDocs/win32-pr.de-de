---
description: Tragbare Windows-Geräte unterstützen die folgenden Aufgaben Eigenschaften.
ms.assetid: 9bd6c2e1-740a-453d-b390-120700af7c93
title: Task Eigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Task
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 829685ac3fa5737356c172ed9e66303b3d6115ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368358"
---
# <a name="task-properties"></a>Task-Eigenschaften

Tragbare Windows-Geräte unterstützen die folgenden Aufgaben Eigenschaften.



| Eigenschaft                         | VarType        | BESCHREIBUNG                                                                                 |
|----------------------------------|----------------|---------------------------------------------------------------------------------------------|
| **WPD- \_ Aufgaben \_ Besitzer**             | **VT \_ LPWSTR** | Der Besitzer der Aufgabe.                                                                      |
| **Ausführung der WPD- \_ Aufgabe in \_ Prozent \_** | **VT \_ UI4**    | Eine Zahl zwischen 0 und 100, die angibt, wie die Aufgabe fertiggestellt wird.                         |
| **Datum der WPD- \_ Task \_ Erinnerung \_**    | **VT- \_ Datum**   | Ein-Wert, der angibt, wann eine Erinnerung gesendet werden soll, um die Aufgabe auszuführen, wenn Sie nicht vollständig ist. |
| **WPD- \_ Task \_ Status**            | **VT \_ LPWSTR** | Eine Zeichen folgen Beschreibung des Status der Aufgabe, z. b. "in Bearbeitung".                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




