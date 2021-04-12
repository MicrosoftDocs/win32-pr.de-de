---
description: Zertifikate werden gemäß Richtlinien erteilt, die Kriterien definieren, die Anforderer erfüllen muss, um ein Zertifikat zu erhalten.
ms.assetid: ad79dc0d-6457-4459-80e6-ab340436ecac
title: Unabhängigkeit der Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0d99b5babeced0fb87d9e603038e23a40859b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346538"
---
# <a name="policy-independence"></a>Unabhängigkeit der Richtlinie

Zertifikate werden gemäß Richtlinien erteilt, die Kriterien definieren, die Anforderer erfüllen muss, um ein Zertifikat zu erhalten. Eine Richtlinie kann beispielsweise sein, dass nur kommerzielle Zertifikate erteilt werden sollen, wenn die Antragsteller ihre Identifikation persönlich darstellen. Eine andere Richtlinie kann [*Anmelde*](../secgloss/c-gly.md) Informationen basierend auf e-Mail-Anforderungen erteilen Eine Agentur, bei der Kreditkarten ausgestellt werden, kann sich für eine Datenbank entscheiden und vor der Ausstellung einer Karte telefonisch Fragen stellen.

Richtlinien werden in Richtlinien Modulen implementiert, die in C++, C oder Visual Basic geschrieben sind. Zertifikat Dienstfunktionen sind von allen Änderungen in der Richtlinie isoliert, die eine Agentur implementieren kann. Änderungen an der Richtlinie können im Code des Server Richtlinien Moduls vollständig implementiert werden. Eine Unternehmens [*Zertifizierungsstelle (Certification Authority*](../secgloss/c-gly.md) , ca) sollte nur das von Microsoft bereitgestellte Enterprise Policy-Modul verwenden.

 

 
