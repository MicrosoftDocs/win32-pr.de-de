---
description: Die Zertifikat Dienste unterstützen Zertifizierungsstellen Hierarchien (Certification Authority, ca).
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Hierarchien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1fe484d752fc7efc7f098aa1cd1af34d88e799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359442"
---
# <a name="hierarchies"></a>Hierarchien

Die Zertifikat Dienste unterstützen Zertifizierungsstellen Hierarchien ( [*Certification Authority*](../secgloss/c-gly.md) , ca). Eine Zertifizierungsstellen [*Hierarchie*](../secgloss/c-gly.md) besteht aus einer Zertifizierungsstelle der obersten Ebene (als Stamm Zertifizierungsstelle bezeichnet) mit einer oder mehreren untergeordneten Zertifizierungsstellen, die von der Stamm Zertifizierungsstelle Zertifikate ausgestellt wurden. Ein mögliches Szenario der Zertifizierungsstellen Hierarchie wäre in einer Organisation mit einer Stamm Zertifizierungsstelle, die zum Ausstellen von Zertifikaten für mehrere untergeordnete Zertifizierungsstellen verwendet wurde. Die untergeordneten ZS können dann Endentitäts Zertifikate ausstellen, z. b. Zertifikate, die für einen Benutzer ausgestellt wurden. Das Zertifikat des Benutzers enthält einen Vertrauensstellungs Pfad für die Zertifizierungsstellen Hierarchie, in diesem Fall das Zertifikat für die ausstellende untergeordnete Zertifizierungsstelle und die Stamm Zertifizierungsstelle.

 

 
