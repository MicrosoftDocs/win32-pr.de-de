---
description: Die Vertrauenswürdigkeit eines digitalen Zertifikats wird mithilfe einer Vertrauens Hierarchie hergestellt.
ms.assetid: 13ee08b4-9c8e-480b-b78d-9472a2d7b566
title: Hierarchie der Vertrauensstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485c721493a93c7ea55b1993345e8168ccab319b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867407"
---
# <a name="hierarchy-of-trust"></a>Hierarchie der Vertrauensstellung

Damit [*digitale Zertifikate*](../secgloss/c-gly.md) wirksam werden, müssen Benutzer von Zertifikaten über einen hohen Vertrauensgrad verfügen. Es gibt Fälle, in denen ein Benutzer dem Aussteller eines Zertifikats nicht vertraut. Dies kann der Fall sein, wenn der Zertifikat Benutzer nie die [*Zertifizierungs*](../secgloss/c-gly.md) Stelle gehört hat und daher nicht mit der Annahme eines Zertifikats von diesem Aussteller bei einem Gesichts Wert unzufrieden ist. Dieses Problem wird im Zertifizierungsprozess durch eine Vertrauens Hierarchie behoben.

Eine Vertrauens Hierarchie beginnt mit mindestens einer Zertifizierungsstelle, die von allen Entitäten in der Zertifikat Kette als vertrauenswürdig eingestuft wird. Dies kann ein interner Zertifizierungsstellen Administrator oder ein externes Unternehmen oder eine externe Organisation sein, das sich auf das Überprüfen von Identitäten und Ausstellen von Zertifikaten spezialisiert hat Diese Autorität wird als Stamm Zertifizierungsstelle [*bezeichnet.*](../secgloss/r-gly.md) Die Stamm Zertifizierungsstelle zertifiziert dann andere Zertifizierungsstellen, die als erstklassige Zertifizierungsstellen bezeichnet werden, die dann Zertifikate ausstellen und auch zusätzliche Zertifizierungsstellen oder eine zweite Ebene zertifizieren können. Diese Situation ist in der folgenden Abbildung dargestellt.

![Hierarchie der Vertrauensstellung](images/trust.png)

Die Identität der Zertifizierungsstelle, die ein Zertifikat ausgibt, ist Teil eines Zertifikats. Diese Zertifizierungsstelle wird als Aussteller des Zertifikats bezeichnet. Wenn der Aussteller eines Zertifikats eine Zertifizierungsstelle der Ebene 1 oder Ebene 2 ist, der Empfänger dieses Zertifikats kann ermitteln, ob der Aussteller des Zertifikats von einer Zertifizierungsstelle auf einer höheren Ebene als gültige Zertifizierungsstelle zertifiziert ist, und dass die Zertifizierungsstelle der höheren Ebene als gültige Zertifizierungsstelle über eine Zertifizierungsstelle auf höherer Ebene zertifiziert ist, bis eine Vertrauenskette zwischen der niedrigsten Zertifizierungsstelle und dem Stammverzeichnis vorhanden ist. Zertifizierungsstelle.

Beispielsweise kann in der obigen Abbildung überprüft werden, ob ca \# 4 von ca 1 als Zertifizierungsstelle zertifiziert wurde \# und dass ca \# 1 von der Stamm Zertifizierungsstelle als Zertifizierungsstelle zertifiziert wurde. Wenn ein Zertifikat von einer Zertifizierungsstelle auf niedrigerer Ebene zusammen mit der verschlüsselten Nachricht weitergegeben wird, werden Informationen zu allen Zertifikaten in seiner Vertrauenskette bis zum Stamm zusammen mit dem Zertifikat weitergegeben.

Die soeben dargestellten Abbildungen und Beschreibungen sind konzeptionell. In der realen Welt wird die Situation der Zertifizierungsstelle weiterentwickelt, und es wurde keine einzige Stamm Zertifizierungsstelle eingerichtet oder akzeptiert. Kurzfristig werden Inseln der Autorität wie in der folgenden Abbildung dargestellt entwickelt.

![Autoritäts Inseln in einer Hierarchie von Vertrauens Stellungen](images/trust2.png)

In der Zeit können die Stamm Inseln, root 1 und Root 2 in der Abbildung, zu einer einzigen Stamm Zertifizierungsstelle werden. An diesem Punkt würde die Situation wieder über eine einzige Stamm Zertifizierungsstelle verfügen. Es ist immer noch zu sehen, wie sich das tatsächliche Bild weiterentwickelt.

 

 
