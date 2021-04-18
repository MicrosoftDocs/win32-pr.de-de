---
description: Alle normalen RSA/SChannel-und Diffie-Hellman/SChannel-Vorgänge verwenden das \_ Schlüsselpaar für den Schlüsselaustausch aus öffentlichem und privatem Schlüssel.
ms.assetid: e12afdbb-7ba8-444e-a43f-e262b481a353
title: Verwendung des öffentlichen/privaten Schlüssel Paars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dba78c487c433875ed23ce3f2f3c87a86b07c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357928"
---
# <a name="publicprivate-key-pair-usage"></a>Verwendung des öffentlichen/privaten Schlüssel Paars

Alle normalen [*RSA*](../secgloss/r-gly.md)-/SChannel [*-und Diffie-Hellman/SChannel-*](../secgloss/d-gly.md)Vorgänge verwenden das \_ Schlüsselpaar für den Schlüsselaustausch aus [*öffentlichem und privatem*](../secgloss/p-gly.md)Schlüssel. Zum Bereitstellen der Server [*Authentifizierung*](../secgloss/a-gly.md)muss die Serverseite von SChannel-Vorgängen Zugriff auf das [*X. 509*](../secgloss/x-gly.md) -Zertifikat haben, das seinen öffentlichen Schlüssel und Zugriff auf den entsprechenden [*privaten Schlüssel*](../secgloss/p-gly.md)enthält. Die Client seitige Ausführung von [*SChannel*](../secgloss/s-gly.md) benötigt das Zertifikat mit seinem öffentlichen Schlüssel und Zugriff auf den privaten Schlüssel, wenn die Client Authentifizierung implementiert ist.

Da SChannel-Protokoll-Engines nie das \_ Schlüsselpaar für öffentliche/private Schlüssel in der Signatur verwenden, muss das Schlüsselpaar nicht von einem neuen CSP unterstützt werden, der nur RSA/SChannel oder Diffie-Hellman/SChannel unterstützt.

Wenn eine Protokoll-Engine eine SSL 3,0-Export Verschlüsselungs Sammlung mit einem- \_ Schlüsselaustausch-Schlüsselpaar verwendet, das größer als 512 Bits ist, muss der Server ein zusätzliches RSA-Schlüsselpaar verwenden. Dieses zusätzliche Schlüsselpaar ist immer genau 512 Bits und kann kurzlebig sein. Das Paar wird als in \_ keyexchange-Element in einem Schlüssel Container gespeichert, der im Besitz der Protokoll-Engine ist. Ein Handle für diesen Schlüssel Container wird in der Regel beim Start der Protokoll-Engine abgerufen.

Diffie-Hellman unterstützt nur [*calg \_ dh \_ ephem*](../secgloss/c-gly.md) und verwendet normale RSA-oder DSS-öffentliche Schlüssel.

 

 
