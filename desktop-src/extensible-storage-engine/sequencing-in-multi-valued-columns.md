---
description: Weitere Informationen finden Sie unter Sequenzierung in mehrwertigen Spalten.
title: Sequenzierung in mehrwertigen Spalten
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 54f4bd7734cb8c1bf5a87eb444c3205d89f4a6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563625"
---
# <a name="sequencing-in-multi-valued-columns"></a>Sequenzierung in mehrwertigen Spalten


_**Gilt für:** Windows | Windows Server_

## <a name="sequencing-in-multi-valued-columns"></a>Sequenzierung in mehrwertigen Spalten

Die Werte in einer mehrwertigen Spalte werden durch eine Indexnummer identifiziert, die als *itagsequence* bezeichnet wird. Diese Zahl ist ein Verweis auf einen einzelnen Wert der Spalte. Diese Zahl wird verwendet, wenn neue Werte in der Spalte festgelegt, abgerufen oder aufgezählt werden. Die *itagsequence* wird in verschiedenen Strukturen verwendet, einschließlich:

  - [JET_RETINFO](./jet-retinfo-structure.md)

  - [JET_SETINFO](./jet-setinfo-structure.md)

  - [JET_SETCOLUMN](./jet-setcolumn-structure.md)

  - [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)

  - [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)

Diese *itagsequence* beginnt bei 1 für jeden Wert in der mehrwertigen Spalte. Die Sequenznummer wird erhöht, wenn der Spalte neue Werte hinzugefügt werden. Wenn Sie einen Wert in einer Spalte mit einer *itagsequence* von 0 festlegen, wird angegeben, dass der Wert an den bereits in dieser Spalte bereits in dieser Spalte bereits angefügten Satz von Werten angefügt werden Die Verwendung einer *itagsequence* -Zahl, die größer als die Anzahl der derzeit für eine Spalte festgelegten Werte ist, hat dieselbe Wirkung. Wenn Sie die *itagsequence* eines vorhandenen Werts angeben, wird dieser Wert überschrieben, und es wird kein neuer Wert eingefügt. Wenn Sie einen vorhandenen Wert auf NULL festlegen, wird dieser Wert aus dem bereits in dieser Spalte vorhandenen Satz von Werten entfernt. Dadurch werden alle nachfolgenden Werte in der Spalte um einen Slot nach unten verschoben, sodass der nachfolgende Zugriff auf diese Werte von *itagsequence* durch eine Zahl kleiner als die zuvor verwendete ist.

Das folgende Diagramm zeigt eine *itagsequence* in einer mehrwertigen Spalte. Die Spalte mit dem Namen "Cola" hat drei Einträge: Wert1, Wert2 und Val3 mit *itagsequence* von 1, 2 und 3.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")
