---
description: Für viele der Funktionen sind Zertifikat-oder Nachrichten Codierungs Typen erforderlich.
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: Zertifikat-und Nachrichten Codierungs Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3193b321d27892f8df9535ef81b8a988bf558e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484694"
---
# <a name="certificate-and-message-encoding-types"></a>Zertifikat-und Nachrichten Codierungs Typen

Für viele der Funktionen sind Zertifikat-oder [*Nachrichten Codierungs Typen*](../secgloss/m-gly.md)erforderlich. Dieser Codierungstyp ist ein **DWORD**, das möglicherweise sowohl den Zertifikat-als auch den Nachrichten Codierungstyp enthält. Der zertifikatcodierungstyp wird im nieder wertigen Wort gespeichert. Der Nachrichten Codierungstyp wird im hohen Bestell Wort gespeichert. Für einige Funktionen oder Struktur Felder ist nur einer der Codierungs Typen erforderlich, aber es ist immer akzeptabel, beide Codierungs Typen anzugeben. Ein Beispiel für die Angabe beider Codierungs Typen finden Sie unter [ \# includes und \# Definitionen](-includes-and--defines.md).

Die folgende Parameter Benennungs Konvention wird verwendet, um die erforderlichen Codierungs Typen anzugeben.



| Name                       | Kommentare                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *dwmsgandcertencodingtype* | Beide Codierungs Typen sind erforderlich.                                                                                                                                                                                                                                                                                       |
| *dwmsgencodingtype*        | Nur der Nachrichten Codierungstyp ist erforderlich.                                                                                                                                                                                                                                                                             |
| *dwcertencodingtype*       | Nur der zertifikatcodierungstyp ist erforderlich.                                                                                                                                                                                                                                                                         |
| *dwencodingtype*           | Es ist entweder ein Nachrichten-oder zertifikatcodierungstyp erforderlich. Wenn das nieder wertige Wort, das den Zertifikat Codierungstyp enthält, nicht NULL ist, wird es verwendet. Andernfalls wird das höchst wertige Wort verwendet, das den Nachrichten Codierungstyp enthält. Wenn beide angegeben werden, wird der Zertifikat Codierungstyp in der nieder wertigen Word verwendet. |



 

Die in der folgenden Tabelle aufgeführten aktuellen Codierungs Typen sind aktuell definiert.



| Codierungstyp          | Wert      |
|------------------------|------------|
| Crypt- \_ ASN- \_ Codierung   | 0x00000001 |
| X509- \_ ASN- \_ Codierung    | 0x00000001 |
| PKCS \_ 7- \_ ASN- \_ Codierung | 0x00010000 |



 

 

 
