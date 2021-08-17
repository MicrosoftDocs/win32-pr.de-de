---
description: Certificate Services unterstützt Zertifizierungsstellenhierarchien.
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: Hierarchien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 240f2f2fc2920db1a67adb18281ad5c1d67fabdb2996ae3aae8342f96b1810c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006298"
---
# <a name="hierarchies"></a>Hierarchien

Certificate Services unterstützt [*Zertifizierungsstellenhierarchien.*](../secgloss/c-gly.md) Eine [*Zertifizierungsstellenhierarchie*](../secgloss/c-gly.md) besteht aus einer Zertifizierungsstelle der obersten Ebene (als Stammzertifizierungsstelle bezeichnet) mit einer oder mehreren untergeordneten Zertifizierungsstellen, die von der Stammzertifizierungsstelle zertifikate ausgestellt wurden. Ein mögliches Szenario für die Zertifizierungsstellenhierarchie wäre eine Organisation mit einer Stammzertifizierungsstelle, die zum Ausstellen von Zertifikaten für mehrere untergeordnete Zertifizierungsstellen verwendet wurde. Die untergeordneten Zertifizierungsstellen können dann Endentitätszertifikate ausstellen, z. B. Zertifikate, die für einen Benutzer ausgestellt wurden. Das Zertifikat des Benutzers enthält einen Vertrauenspfad für die Zertifizierungsstellenhierarchie, in diesem Fall einschließlich des Zertifikats für die ausstellende untergeordnete Zertifizierungsstelle und die Stammzertifizierungsstelle.

 

 
