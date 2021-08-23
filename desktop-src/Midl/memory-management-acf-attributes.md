---
title: ACF-Attribute für die Speicherverwaltung
description: Mit den in der folgenden Tabelle aufgeführten Attributen können Sie die Speicherverwaltung auf Clientseite durchführen.
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- ACF MIDL , Attribute, Speicherverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d7df6f020d8531f0c1ca8bebdd6bf59270f2ed22c821e2c183c9da6936e306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013748"
---
# <a name="memory-management-acf-attributes"></a>ACF-Attribute für die Speicherverwaltung

Mit den in der folgenden Tabelle aufgeführten Attributen können Sie die Speicherverwaltung auf Clientseite durchführen.



| attribute                                   | Verbrauch                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**allocate**](allocate.md)                | Gibt an, wie die Clientanwendung und der Stub Speicher für Zeiger zuordnen und freigibt. Dieses Attribut ist besonders nützlich, wenn bestimmte Zeigerstrukturen für die Serveranwendung zugänglich bleiben, nachdem der Remoteprozeduraufruf an den Client zurückgegeben wurde. Sie können auch das [**Attribut allocate**](allocate.md) verwenden, um den Stub an die Berechnung der Größe des arbeitsspeichers zu richten, auf den über den Zeiger des angegebenen Typs verwiesen wird, und um einen einzelnen Aufruf von midl user [**zu \_ \_ verwenden.**](/windows/desktop/Rpc/the-midl-user-allocate-function) |
| [**\_Byteanzahl**](byte-count.md)           | Ermöglicht das Erstellen eines persistenten, zusammenhängenden Speicherblocks, der über mehrere Remoteprozeduraufrufe wiederverwendet werden kann. Dadurch entlädt sich für die Clientanwendung der Mehraufwand der wiederholten Zuweisung und Freigabe von Arbeitsspeicher, der mehrere Zeiger und andere komplexe Datenstrukturen enthalten kann.                                                                                                                                                                                                                                                      |
| [**\_"Allocate" aktivieren**](enable-allocate.md) | Gibt an, dass der Serverstubcode die Stubspeicherverwaltungsumgebung aktivieren soll.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 