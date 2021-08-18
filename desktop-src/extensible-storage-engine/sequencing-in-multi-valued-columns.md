---
description: Weitere Informationen finden Sie unter Sequenzieren in mehrwertigen Spalten.
title: Sequenzieren in mehrwertigen Spalten
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 45c8c192becdb616b94360b491bd66f9e6fa492542da320a5536527c2bd45605
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016020"
---
# <a name="sequencing-in-multi-valued-columns"></a>Sequenzieren in mehrwertigen Spalten


_**Gilt für:** Windows | Windows Server_

## <a name="sequencing-in-multi-valued-columns"></a>Sequenzieren in mehrwertigen Spalten

Die Werte in einer mehrwertigen Spalte werden durch eine Indexnummer namens *itagSequence* identifiziert. Diese Zahl ist ein Verweis auf einen einzelnen Wert der Spalte. Diese Zahl wird verwendet, wenn neue Werte in der Spalte festgelegt, abgerufen oder aufgezählt werden. *ItagSequence* wird in verschiedenen Strukturen verwendet, einschließlich:

  - [JET_RETINFO](./jet-retinfo-structure.md)

  - [JET_SETINFO](./jet-setinfo-structure.md)

  - [JET_SETCOLUMN](./jet-setcolumn-structure.md)

  - [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)

  - [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)

Diese *ItagSequence* beginnt bei 1 für jeden Wert in der mehrwertigen Spalte. Die Sequenznummer wird erhöht, wenn der Spalte neue Werte hinzugefügt werden. Das Festlegen eines Werts in einer Spalte mit dem *Wert itagSequence* von 0 gibt an, dass der Wert an den Satz von Werten angefügt werden soll, die sich bereits in dieser Spalte befinden. Die Verwendung eines *ItagSequence-Werts,* der größer ist als die Anzahl der derzeit für eine Spalte festgelegten Werte, hat die gleiche Auswirkung. Wenn Sie die *ItagSequence* eines vorhandenen Werts angeben, wird dieser Wert überschrieben, und es wird kein neuer Wert eingefügt. Wenn Sie einen vorhandenen Wert auf NULL festlegen, wird dieser Wert aus dem Satz von Werten entfernt, die sich bereits in dieser Spalte befinden. Dadurch werden alle nachfolgenden Werte in der Spalte um einen Slot nach unten verschoben, sodass der nachfolgende Zugriff auf diese Werte durch *itagSequence* um eine Zahl 1 kleiner als die zuvor verwendete ist.

Das folgende Diagramm zeigt eine *itagSequence* in einer mehrwertigen Spalte. Die Spalte namens ColA weist drei Einträge auf: Val1, Val2 und Val3 mit *itagSequence* von 1, 2 bzw. 3.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")
