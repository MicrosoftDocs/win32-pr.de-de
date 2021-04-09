---
description: Ein &\# 0034; Eingabe Kontext&\# 0034; ist eine interne Struktur, die vom imm verwaltet wird.
ms.assetid: 2b639e30-5368-45bb-943d-db1ab6b62582
title: Eingabe Kontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f1f83a397373e17a7d637b61a3232a3d72acde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864880"
---
# <a name="input-context"></a>Eingabe Kontext

Ein "Eingabe Kontext" ist eine interne Struktur, die vom imm verwaltet wird. Sie enthält Informationen zum Status von IME und wird von IME-Fenstern verwendet. Standardmäßig erstellt das Betriebssystem jedem Thread einen Eingabe Kontext und weist ihn zu. Innerhalb des Threads handelt es sich bei diesem Standardeingabe Kontext um eine freigegebene Ressource, die mit jedem neu erstellten Fenster verknüpft ist.

Zum Abrufen oder Festlegen von Informationen im IME muss eine IME-fähige Anwendung zunächst ein Handle für den Eingabe Kontext abrufen, der einem angegebenen Fenster zugeordnet ist. Die Anwendung ruft das Handle mithilfe der [**immgetcontext**](/windows/desktop/api/Imm/nf-imm-immgetcontext) -Funktion ab. Sie kann das abgerufene Handle in nachfolgenden Aufrufen der imm-Funktionen verwenden, um IME-Werte abzurufen und festzulegen, z. b. den Stil des Kompositions Fensters, den Kompositionsstil und die Statusfenster Position. Nachdem die Anwendung die Verwendung des Kontexts abgeschlossen hat, muss Sie den Kontext mithilfe der [**immreleasecontext**](/windows/desktop/api/Imm/nf-imm-immreleasecontext) -Funktion freigeben.

Da der Standardeingabe Kontext eine freigegebene Ressource ist, gelten alle Änderungen, die die Anwendung daran vornimmt, für alle Fenster im Thread. Die Anwendung kann dieses Standardverhalten jedoch überschreiben, indem Sie Ihren eigenen Eingabe Kontext erstellt und einem oder mehreren Fenstern des Threads zuordnet. Die an einem anwendungsspezifischen Eingabe Kontext vorgenommenen Änderungen gelten nur für die Fenster, die dem Kontext zugeordnet sind.

Die Anwendung kann mithilfe der [**immkreatecontext**](/windows/desktop/api/Imm/nf-imm-immcreatecontext) -Funktion einen Eingabe Kontext erstellen. Um den Kontext einem Fenster zuzuweisen, ruft die Anwendung die [**immassociatecontext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) -Funktion auf. Diese Funktion gibt ein Handle für den zuvor zugeordneten Eingabe Kontext zurück. Wenn die Anwendung nicht bereits einen Eingabe Kontext mit dem Fenster verknüpft hat, ist das zurückgegebene Handle für den Standardeingabe Kontext. In der Regel speichert die Anwendung dieses Handle und ordnet sie später dem Fenster zu, wenn der angepasste Eingabe Kontext nicht mehr benötigt wird.

Sobald ein Eingabe Kontext einem Fenster zugeordnet ist, wählt das Betriebssystem automatisch diesen Kontext aus, wenn das Fenster aktiviert wird, und empfängt den Eingabefokus. Der Stil und andere Informationen im Eingabe Kontext beeinflussen die nachfolgende Tastatureingabe für dieses Fenster, um zu bestimmen, wie der IME funktioniert.

Die Anwendung muss alle benutzerdefinierten Eingabe Kontexte zerstören, bevor Sie beendet wird. Zuerst entfernt die Anwendung den Eingabe Kontext aus jeder Zuordnung, die Sie mit Windows im Thread erstellt hat, mithilfe der [**immassociatecontext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) -Funktion. Anschließend wird die Funktion " [**immdestroycontext**](/windows/desktop/api/Imm/nf-imm-immdestroycontext) " aufgerufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über den Eingabemethoden-Manager](about-input-method-manager.md)
</dt> </dl>

 

 



