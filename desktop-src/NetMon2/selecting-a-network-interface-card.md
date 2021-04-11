---
description: Netzwerkmonitor bietet drei Funktionen zum Auswählen einer Netzwerkschnittstellenkarte (NIC). Diese Funktionen bieten drei Möglichkeiten zum Auflisten eines Satzes von NICs und zum Auswählen des zu verwendenden NICs. In der folgenden Tabelle sind diese Funktionen aufgeführt.
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: Auswählen einer Netzwerkschnittstellenkarte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8315a97cc8457d86614fc25c87c39b1b9794c7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131192"
---
# <a name="selecting-a-network-interface-card"></a>Auswählen einer Netzwerkschnittstellenkarte

Netzwerkmonitor bietet drei Funktionen zum Auswählen einer Netzwerkschnittstellenkarte (NIC). Diese Funktionen bieten drei Möglichkeiten zum Auflisten eines Satzes von NICs und zum Auswählen des zu verwendenden NICs. In der folgenden Tabelle sind diese Funktionen aufgeführt.



| Funktion                                                 | BESCHREIBUNG                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getnppblobfromui**](getnppblobfromui.md)             | Verwendet die Netzwerkmonitor-Benutzeroberfläche, um die registrierten NICs anzuzeigen, und gibt das NPP-BLOB zurück, das die NIC darstellt, an der Sie interessiert sind.           |
| [**Getnppblobtable**](getnppblobtable.md)               | Gibt eine BLOB-Tabelle zurück. Die Anwendung muss die Tabelle auflisten und einen NPP-BLOB auswählen.                                                       |
| [**Selectnppblobfromtable**](selectnppblobfromtable.md) | Verwendet die Netzwerkmonitor-Schnittstelle, um die angegebenen NPP-BLOBs anzuzeigen, und gibt das NPP-BLOB zurück, das die NIC darstellt, an der Sie interessiert sind. |



 

Jede NIC wird durch einen NPP-Binary Large Object (BLOB) dargestellt. Diese Funktionen können ein einzelnes NPP-BLOB von den auf dem Computer registrierten, einem einzelnen NPP-BLOB aus einer bereitgestellten NPP-BLOB-Tabelle oder einer Tabelle mit NPP-BLOBs zurückgeben, die der Aufrufer dann verwenden muss, um ein bestimmtes BLOB auszuwählen. In den ersten beiden Fällen zeigt die Netzwerkmonitor-Benutzeroberfläche bei der Auswahl aus den registrierten NICs oder einer bereitgestellten NPP-BLOB-Tabelle die NICs an, die Sie auswählen können.

> [!Note]  
> Netzwerkmonitor verwendet eine Funktion mit dem Namen NPP Finder, um die auf dem lokalen Computer registrierten NICs aufzuzählen. Der NPP-Finder ist eine Komponente von Npptools.dll.

 



| Informationen über                            | Finden Sie unter                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Auswählen einer auf dem lokalen Computer registrierten NIC | [Auswählen einer registrierten NIC](selecting-a-registered-nic.md)                                         |
| Auswählen einer NIC aus einer angegebenen NPP-BLOB-Tabelle   | [Auswählen einer NIC aus einer angegebenen NPP-BLOB-Tabelle](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| Abrufen einer NPP-BLOB-Tabelle                     | [Auswählen einer NIC aus einer zurückgegebenen NPP-BLOB-Tabelle](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



