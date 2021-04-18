---
description: Mithilfe des Verwaltungs Programms Komponenten Dienste können Sie in anwendungsspezifische Komponenten importieren, die bereits als COM-Komponenten in der Windows-Registrierung auf Ihrem Computer registriert wurden.
ms.assetid: 5310e08a-5146-41f8-ae65-8467b921abd4
title: Importieren von Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b67d944e9b8880b3edd0583569155fffecb23b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483035"
---
# <a name="importing-components"></a>Importieren von Komponenten

Mithilfe des Verwaltungs Programms Komponenten Dienste können Sie in anwendungsspezifische Komponenten importieren, die bereits als COM-Komponenten in der Windows-Registrierung auf Ihrem Computer registriert wurden. Beim Importieren einer Komponente werden die Schnittstellen-oder Methoden Informationen, die zum Festlegen von Schnittstelleneigenschaften oder zum Konfigurieren des Zugriffs auf die Komponente von einem Remote Client benötigt werden, nicht installiert. Daher sollten Sie, wenn möglich, installieren, anstatt nicht konfigurierte Komponenten zu importieren.

> [!Note]  
> Beim Importieren einer Komponente in eine COM+-Anwendung füllt com+ keine Schnittstellen-und Methoden Informationen für die Komponente auf. Beim Exportieren eines Anwendungs Proxys stellt com+ keine Marshallinginformationen (Typbibliotheken oder Proxy/stusb) für einige oder alle Schnittstellen bereit. Das Exportieren von Anwendungs Proxys, die importierte Komponenten enthalten, schlägt fehl oder bewirkt, dass eine Warnung ausgegeben wird.

 

**So importieren Sie eine Komponente in eine COM+-Anwendung**

1.  Wählen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste den Computer aus, auf dem die COM+-Anwendung gehostet wird.

2.  Öffnen Sie den Ordner **com+-Anwendungen** für diesen Computer, und wählen Sie die Anwendung aus, in der die Komponente installiert werden soll.

3.  Öffnen Sie den Anwendungsordner, und wählen Sie **Komponenten** aus.

4.  Zeigen Sie im Menü **Aktion** auf **neu**, und klicken Sie dann auf **Komponente**. Sie können auch mit der rechten Maustaste auf den Ordner **Komponenten** , zeigen Sie auf **neu**, und klicken Sie dann auf **Komponente**.

5.  Klicken Sie auf der **Willkommens** Seite des COM+-Anwendungsinstallations-Assistenten auf **weiter**, und klicken Sie dann im Dialogfeld **Komponente importieren oder installieren** auf die **Komponente (en) importieren, die bereits registriert sind**.

6.  Aktivieren Sie im Dialogfeld **zu importierende Komponenten auswählen** das Kontrollkästchen **Details** , um die gesamten Informationen zu den bereits registrierten Komponenten anzuzeigen. Wählen Sie die zu importierenden Komponenten aus der angezeigten Liste aus, und klicken Sie auf **weiter**.

7.  Klicken Sie auf **Fertig stellen**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kopieren von Komponenten](copying-components.md)
</dt> <dt>

[Eine neue COM+-Anwendung wird erstellt.](creating-a-new-com--application.md)
</dt> <dt>

[Eine COM+-Anwendung wird gelöscht.](deleting-a-com--application.md)
</dt> <dt>

[Installieren neuer Komponenten](installing-new-components.md)
</dt> <dt>

[Verschieben von Komponenten](moving-components.md)
</dt> <dt>

[Entfernen einer Komponente aus einer COM+-Anwendung](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



