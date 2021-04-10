---
title: ACF-Attribute für die Speicherverwaltung
description: Mithilfe der in der folgenden Tabelle aufgeführten Attribute können Sie die Arbeitsspeicher Verwaltung von der Clientseite aus durchführen.
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- ACF-Mittell, Attribute, Speicherverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12a0ee6d11a2b10e1c0fad7cd1a42411670b508
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948686"
---
# <a name="memory-management-acf-attributes"></a>ACF-Attribute für die Speicherverwaltung

Mithilfe der in der folgenden Tabelle aufgeführten Attribute können Sie die Arbeitsspeicher Verwaltung von der Clientseite aus durchführen.



| Attribut                                   | Verbrauch                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**allocate**](allocate.md)                | Gibt an, wie die Client Anwendung und der Stub Speicher für Zeiger zuweisen und freigeben. Dieses Attribut ist besonders nützlich, wenn Sie möchten, dass bestimmte Zeiger Strukturen für die Serveranwendung zugänglich bleiben, nachdem der Remote Prozedur Aufruf an den Client zurückgegeben wurde. Sie können auch das Attribut " [**zuordnen**](allocate.md) " verwenden, um den Stub anzuweisen, die Größe des gesamten Speichers zu berechnen, auf den über den Zeiger des angegebenen Typs verwiesen wird, und einen einzelnen aufzurufenden [**Mittel l- \_ Benutzer \_ zuzuordnen**](/windows/desktop/Rpc/the-midl-user-allocate-function). |
| [**Byte \_ Anzahl**](byte-count.md)           | Ermöglicht es Ihnen, einen permanenten, zusammenhängenden Speicherblock zu erstellen, der über mehrere Remote Prozedur Aufrufe wieder verwendet werden kann. Dadurch wird die Client Anwendung vom mehr Aufwand für das wiederholte Zuweisen und Freigeben von Arbeitsspeicher, der mehrere Zeiger und andere komplexe Datenstrukturen enthalten kann, freigegeben.                                                                                                                                                                                                                                                      |
| [**\_zuordnen aktivieren**](enable-allocate.md) | Gibt an, dass der Serverstub-Code die Stub-Speicher Verwaltungs Umgebung aktivieren soll.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 