---
description: Sitzungsschlüssel sind Schlüssel, die generiert werden, damit Sie in einer einzelnen Kommunikationssitzung verwendet werden können.
ms.assetid: 18bf2023-084d-400d-b60d-1ba51ce6a2bc
title: Sitzungsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4089f9ab5a0ae6889463c1b24c2eecb376c7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369808"
---
# <a name="session-keys"></a>Sitzungsschlüssel

[*Sitzungsschlüssel*](../secgloss/s-gly.md) sind Schlüssel, die generiert werden, damit Sie in einer einzelnen Kommunikationssitzung verwendet werden können. Sitzungsschlüssel werden häufig geändert und verworfen, wenn Sie nicht mehr benötigt werden. TLS verwendet beispielsweise für jede Verbindung einen separaten Sitzungsschlüssel, und S/MIME verwendet für jede e-Mail-Nachricht einen separaten Sitzungsschlüssel. In der Regel wird ein [*symmetrischer Schlüssel*](../secgloss/s-gly.md) als Sitzungsschlüssel verwendet.

Sitzungsschlüssel sind flüchtig. Anwendungen können diese Schlüssel zur späteren Verwendung oder zur Übertragung an andere Benutzer speichern. Weitere Informationen finden Sie unter [kryptografieschlüsselspeicher und Exchange](cryptographic-key-storage-and-exchange.md).

 

 
