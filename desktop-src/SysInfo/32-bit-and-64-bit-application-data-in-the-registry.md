---
description: Auf 64-Bit-Windows werden Teile der Registrierungseinträge separat für 32-Bit-Anwendungen und 64-Bit-Anwendungen gespeichert und mithilfe des Registrierungsumleitungs- und Registrierungsreflektions in separaten logischen Registrierungssichten zugeordnet, da die 64-Bit-Version einer Anwendung möglicherweise andere Registrierungsschlüssel und -werte als die 32-Bit-Version verwendet. Es gibt auch freigegebene Registrierungsschlüssel, die nicht umgeleitet oder widergespiegelt werden.
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: 32-Bit- und 64-Bit-Anwendungsdaten in der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87d5177eb48a5497e321b47bb0da96874a0e6522360f2dc519dc72df3dcdf89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764984"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a>32-Bit- und 64-Bit-Anwendungsdaten in der Registrierung

Auf 64-Bit-Windows werden Teile der Registrierungseinträge separat für 32-Bit-Anwendungen und 64-Bit-Anwendungen gespeichert und mithilfe des [Registrierungsumleitungs-](/windows/desktop/WinProg64/registry-redirector) und [Registrierungsreflektions](/windows/desktop/WinProg64/registry-reflection)in separaten logischen Registrierungssichten zugeordnet, da die 64-Bit-Version einer Anwendung möglicherweise andere Registrierungsschlüssel und -werte als die 32-Bit-Version verwendet. Es gibt auch [freigegebene Registrierungsschlüssel,](/windows/desktop/WinProg64/shared-registry-keys) die nicht umgeleitet oder widergespiegelt werden.

Das übergeordnete Element jedes 64-Bit-Registrierungsknotens ist der Image-Specific Node oder ISN. Der Registrierungs-Redirector leitet den Registrierungszugriff einer Anwendung transparent an den entsprechenden ISN-Unterknoten weiter. Umleitungsunterknoten in der Registrierungsstruktur werden automatisch von der WOW64-Komponente mit dem Namen **Wow6432Node** erstellt. Daher ist es wichtig, keinen Registrierungsschlüssel zu benennen, den Sie erstellen **Wow6432Node.**

Die \_ Flags KEY WOW64 \_ 64KEY und KEY \_ WOW64 \_ 32KEY ermöglichen den expliziten Zugriff auf die 64-Bit-Registrierungsansicht bzw. die 32-Bit-Ansicht. Weitere Informationen finden Sie unter [Zugreifen auf eine alternative Registrierungsansicht.](/windows/desktop/WinProg64/accessing-an-alternate-registry-view)

Verwenden Sie zum Deaktivieren und Aktivieren der Registrierungsreflektion für einen bestimmten Schlüssel die Funktionen [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) und [**RegEnableReflectionKey.**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) Anwendungen sollten die Reflektion nur für die Registrierungsschlüssel deaktivieren, die sie erstellen, und nicht versuchen, die Reflektion für die vordefinierten Schlüssel wie **HKEY \_ LOCAL \_ MACHINE** oder **HKEY \_ CURRENT \_ USER** zu deaktivieren. Verwenden Sie die [**RegQueryReflectionKey-Funktion,**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) um zu bestimmen, welche Schlüssel in der Reflektionsliste enthalten sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierungs-Redirector](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[Registrierungsreflektion](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
