---
description: Netzwerkmonitor stellt drei Funktionen zum Auswählen einer Netzwerkschnittstellenkarte (NIC) bereit. Diese Funktionen bieten drei Möglichkeiten, eine Gruppe von NICs zu aufzählen und die zu verwendende auszuwählen. In der folgenden Tabelle sind diese Funktionen aufgeführt.
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: Auswählen einer Netzwerkschnittstellenkarte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f93341bb169f2672579ac6764186925b7190f1ac52c698e2426e1c20d3e854
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074490"
---
# <a name="selecting-a-network-interface-card"></a>Auswählen einer Netzwerkschnittstellenkarte

Netzwerkmonitor stellt drei Funktionen zum Auswählen einer Netzwerkschnittstellenkarte (NIC) bereit. Diese Funktionen bieten drei Möglichkeiten, eine Gruppe von NICs zu aufzählen und die zu verwendende auszuwählen. In der folgenden Tabelle sind diese Funktionen aufgeführt.



| Funktion                                                 | BESCHREIBUNG                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetNPPBlobFromUI**](getnppblobfromui.md)             | Verwendet die Netzwerkmonitor-Benutzeroberfläche, um die registrierten NICs anzuzeigen, und gibt das NPP-BLOB zurück, das die NIC darstellt, an der Sie interessiert sind.           |
| [**GetNPPBlobTable**](getnppblobtable.md)               | Gibt eine BLOB-Tabelle zurück. Die Anwendung muss die Tabelle aufzählen und ein NPP-BLOB auswählen.                                                       |
| [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) | Verwendet die Netzwerkmonitor-Schnittstelle, um die bereitgestellten NPP-BLOBs anzuzeigen, und gibt das NPP-BLOB zurück, das die NIC darstellt, an der Sie interessiert sind. |



 

Jede NIC wird durch ein BLOB (Binary Large Object) von NPP dargestellt. Diese Funktionen können ein einzelnes NPP-BLOB von den auf dem Computer registrierten Blobs, ein einzelnes NPP-BLOB aus einer angegebenen NPP-BLOB-Tabelle oder eine Tabelle mit NPP-BLOBs zurückgeben, die der Aufrufer dann verwenden muss, um ein bestimmtes BLOB auszuwählen. In den ersten beiden Fällen zeigt die Netzwerkmonitor-Benutzeroberfläche die NICs an, die Sie auswählen können, wenn Sie aus den registrierten NICs oder aus einer angegebenen NPP-BLOB-Tabelle auswählen.

> [!Note]  
> Netzwerkmonitor verwendet ein Feature namens NPP Finder, um die auf dem lokalen Computer registrierten NICs aufzählen. Der NPP-Finder ist eine Komponente von Npptools.dll.

 



| Informationen über                            | Finden Sie unter                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Auswählen einer auf dem lokalen Computer registrierten NIC | [Auswählen einer registrierten NIC](selecting-a-registered-nic.md)                                         |
| Auswählen einer NIC aus einer angegebenen NPP-BLOB-Tabelle   | [Auswählen einer NIC aus einer angegebenen NPP-BLOB-Tabelle](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| Abrufen einer NPP-BLOB-Tabelle                     | [Auswählen einer NIC aus einer zurückgegebenen NPP-BLOB-Tabelle](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



