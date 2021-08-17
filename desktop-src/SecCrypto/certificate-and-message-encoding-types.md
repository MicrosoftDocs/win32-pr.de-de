---
description: Viele der Funktionen erfordern Zertifikat- oder Nachrichtencodierungstypen.
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: Zertifikat- und Nachrichtencodierungstypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185be8d3cc781786c93ac809c042c86d3601a45d86eaa39452f0bcbf44203a1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771976"
---
# <a name="certificate-and-message-encoding-types"></a>Zertifikat- und Nachrichtencodierungstypen

Viele der Funktionen erfordern zertifikat- oder [*nachrichtencodierungstypen.*](../secgloss/m-gly.md) Dieser Codierungstyp ist ein **DWORD-Typ,** der möglicherweise sowohl den Zertifikat- als auch den Nachrichtencodierungstyp enthält. Der Zertifikatcodierungstyp wird im Wort der niedrigen Ordnung gespeichert. Der Nachrichtencodierungstyp wird im hohen Wort gespeichert. Einige Funktionen oder Strukturfelder erfordern nur einen der Codierungstypen, aber es ist immer akzeptabel, beide Codierungstypen anzugeben. Ein Beispiel für die Angabe beider Codierungstypen finden Sie unter [ \# includes und \# defines](-includes-and--defines.md).

Die folgende Parameterbenennungskonvention wird verwendet, um die erforderlichen Codierungstypen anzugeben.



| Name                       | Kommentare                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *dwMsgAndCertEncodingType* | Beide Codierungstypen sind erforderlich.                                                                                                                                                                                                                                                                                       |
| *dwMsgEncodingType*        | Nur der Nachrichtencodierungstyp ist erforderlich.                                                                                                                                                                                                                                                                             |
| *dwCertEncodingType*       | Nur der Zertifikatcodierungstyp ist erforderlich.                                                                                                                                                                                                                                                                         |
| *dwEncodingType*           | Es ist entweder ein Nachrichten- oder Zertifikatcodierungstyp erforderlich. Wenn das niedrig geordnete Wort, das den Zertifikatcodierungstyp enthält, ungleich 0 (null) ist, wird es verwendet. Andernfalls wird das hohe Wort verwendet, das den Nachrichtencodierungstyp enthält. Wenn beide angegeben sind, wird der Zertifikatcodierungstyp im niedrig geordneten Wort verwendet. |



 

Derzeit definierte Codierungstypen sind in der folgenden Tabelle aufgeführt.



| Codierungstyp          | Wert      |
|------------------------|------------|
| CRYPT \_ \_ ASN-CODIERUNG   | 0x00000001 |
| \_X509-ASN-CODIERUNG \_    | 0x00000001 |
| PKCS \_ 7 \_ ASN-CODIERUNG \_ | 0x00010000 |



 

 

 
