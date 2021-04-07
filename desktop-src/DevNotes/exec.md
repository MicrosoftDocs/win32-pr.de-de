---
description: HKLM \\ Software \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2711b2c8882f9af12de2f060810ccd4219faa5ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748760"
---
# <a name="exec"></a>Exec

**HKLM \\ Software \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**



| Datentyp | Range                    | Standardwert |
|-----------|--------------------------|---------------|
| REG- \_ SZ   | *Pfad zur ausführbaren Datei* |               |



 

## <a name="browser-integration-steps"></a>Schritte zur Browser Integration

1.  Verwenden Sie die [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) -Funktion, um zu bestimmen, ob die Netzwerk Diagnose installiert ist. Wenn Sie installiert ist, ist der Schlüssel **{e2e2dd38-d088-4134-82b7-f2ba38496583}** vorhanden.
2.  Verwenden Sie die [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) -Funktion, um den Pfad der ausführbaren Datei für die Netzwerk Diagnose aus dem **exec** -Eintrag abzurufen.
3.  Zeigen Sie die neue Fehlerseite an, wenn die Diagnose auf dem System installiert ist.
4.  Erstellen Sie eine Browser Erweiterung, mit der ein Standard Symbolleisten Element erstellt wird, wenn die Diagnose auf dem System installiert ist.
5.  Führen Sie die ausführbare Datei für die Netzwerk Diagnose mit dem in Schritt 2 abgerufenen Pfad aus

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Features der Netzwerk Diagnose Tools](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 
