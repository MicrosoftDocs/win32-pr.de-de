---
description: HKLM \\ Software Microsoft Internet Explorer Extensions \\ \\ \\ \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93228857af2e531360b6238ab649daf8ac3f9eb2acf0aecfb12348b0ed990b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795240"
---
# <a name="exec"></a>Exec

**HKLM \\ Software Microsoft Internet Explorer Extensions \\ \\ \\ \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**



| Datentyp | Range                    | Standardwert |
|-----------|--------------------------|---------------|
| REG \_ SZ   | *Pfad zur ausführbaren Datei* |               |



 

## <a name="browser-integration-steps"></a>Schritte zur Browserintegration

1.  Verwenden Sie [**die RegOpenKeyEx-Funktion,**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) um zu bestimmen, ob die Netzwerkdiagnose installiert ist. Wenn sie installiert ist, ist der **Schlüssel {e2e2dd38-d088-4134-82b7-f2ba38496583}** vorhanden.
2.  Verwenden Sie die [**RegQueryValueEx-Funktion,**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) um den Pfad der ausführbaren Datei für die Netzwerkdiagnose aus dem **Eintrag Exec** abzurufen.
3.  Zeigt die neue Fehlerseite an, wenn die Diagnose auf dem System installiert ist.
4.  Erstellen Sie eine Browsererweiterung, die ein Standardsymbolleistenelement erstellt, wenn die Diagnose auf dem System installiert ist.
5.  Führen Sie die ausführbare Datei für die Netzwerkdiagnose unter Verwendung des in Schritt 2 abgerufenen Pfads aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über das Feature "Netzwerkdiagnosetools"](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 
