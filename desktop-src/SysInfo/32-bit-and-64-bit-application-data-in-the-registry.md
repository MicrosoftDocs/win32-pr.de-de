---
description: Auf 64-Bit-Fenstern werden Teile der Registrierungseinträge separat für die 32-Bit-Anwendung und 64-Bit-Anwendungen gespeichert und mithilfe des registrierungsredirectors und der Registrierungs Reflektion separaten logischen Registrierungs Sichten zugeordnet, da die 64-Bit-Version einer Anwendung andere Registrierungsschlüssel und-Werte als die 32-Bit-Version verwenden kann. Es gibt auch freigegebene Registrierungsschlüssel, die nicht umgeleitet oder reflektiert werden.
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: 32-Bit-und 64-Bit-Anwendungsdaten in der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc82dfbf9b22cf90866e13109aeea2bcdb10e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865396"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a>32-Bit-und 64-Bit-Anwendungsdaten in der Registrierung

Auf 64-Bit-Fenstern werden Teile der Registrierungseinträge separat für die 32-Bit-Anwendung und 64-Bit-Anwendungen gespeichert und mithilfe des [registrierungsredirectors](/windows/desktop/WinProg64/registry-redirector) und der [Registrierungs Reflektion](/windows/desktop/WinProg64/registry-reflection)separaten logischen Registrierungs Sichten zugeordnet, da die 64-Bit-Version einer Anwendung andere Registrierungsschlüssel und-Werte als die 32-Bit-Version verwenden kann. Es gibt auch frei [gegebene Registrierungsschlüssel](/windows/desktop/WinProg64/shared-registry-keys) , die nicht umgeleitet oder reflektiert werden.

Das übergeordnete Element der einzelnen 64-Bit-Registrierungs Knoten ist der Image-Specific Knoten oder isn. Der Registrierungs Redirector leitet den Registrierungs Zugriff einer Anwendung auf den entsprechenden isn-unter Knoten transparent um. Umleitungs unter Knoten in der Registrierungs Struktur werden automatisch von der WOW64-Komponente mit dem Namen **Wow6432Node** erstellt. Daher ist es von entscheidender Bedeutung, keinen Registrierungsschlüssel zu benennen, den Sie **Wow6432Node** erstellen.

Die \_ Flags Key WOW64 \_ 64key und Key \_ WOW64 \_ 32key ermöglichen expliziten Zugriff auf die 64-Bit-Registrierungs Ansicht bzw. die 32-Bit-Sicht. Weitere Informationen finden Sie unter [zugreifen auf eine Alternative Registrierungs Ansicht](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).

Um die Registrierungs Reflektion für einen bestimmten Schlüssel zu deaktivieren und zu aktivieren, verwenden Sie die Funktionen [**regdisablereflectionkey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) und [**regenablereflectionkey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) . Anwendungen sollten die Reflektion nur für die von Ihnen erstellten Registrierungsschlüssel deaktivieren und nicht versuchen, die Reflektion für die vordefinierten Schlüssel zu deaktivieren, wie z. b. **HKEY \_ local \_ Machine** oder **HKEY \_ Current \_ User**. Verwenden Sie die [**regqueryreflectionkey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) -Funktion, um zu bestimmen, welche Schlüssel in der reflektionsliste enthalten sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierungs Redirector](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[Registrierungs Reflektion](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
