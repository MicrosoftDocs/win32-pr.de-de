---
description: Ein &\# 0034;Eingabekontext&0034; ist eine interne Struktur, die vom \# IMM verwaltet wird.
ms.assetid: 2b639e30-5368-45bb-943d-db1ab6b62582
title: Eingabekontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2927d3f573704aadb1ef72bdb26a35d37d90c1f90ab58d3a947ee84f8f38f7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145899"
---
# <a name="input-context"></a>Eingabekontext

Ein "Eingabekontext" ist eine interne Struktur, die vom IMM verwaltet wird. Sie enthält Informationen zum Status des IME und wird von IME-Fenstern verwendet. Standardmäßig erstellt das Betriebssystem einen Eingabekontext und weist diesen jedem Thread zu. Innerhalb des Threads ist dieser Standardeingabekontext eine freigegebene Ressource und wird jedem neu erstellten Fenster zugeordnet.

Um Informationen im IME abzurufen oder festzulegen, muss eine IME-orientierte Anwendung zunächst ein Handle für den Eingabekontext abrufen, der einem angegebenen Fenster zugeordnet ist. Die Anwendung ruft das Handle mithilfe der [**ImmGetContext-Funktion**](/windows/desktop/api/Imm/nf-imm-immgetcontext) ab. Sie kann das abgerufene Handle in nachfolgenden Aufrufen der IMM-Funktionen verwenden, um IME-Werte abzurufen und zu festlegen, z. B. den Kompositionsfensterstil, den Kompositionsstil und die Position des Statusfensters. Nachdem die Anwendung den Kontext verwendet hat, muss sie den Kontext mithilfe der [**ImmReleaseContext-Funktion**](/windows/desktop/api/Imm/nf-imm-immreleasecontext) wieder frei geben.

Da der Standardeingabekontext eine freigegebene Ressource ist, gelten alle Änderungen, die von der Anwendung an ihm vorgenommen werden, für alle Fenster im Thread. Die Anwendung kann dieses Standardverhalten jedoch überschreiben, indem sie einen eigenen Eingabekontext erstellt und einem oder mehr Fenstern des Threads zuschreibt. Die an einem anwendungsspezifischen Eingabekontext vorgenommenen Änderungen gelten nur für die Fenster, die dem Kontext zugeordnet sind.

Ihre Anwendung kann mithilfe der [**ImmCreateContext-Funktion einen Eingabekontext**](/windows/desktop/api/Imm/nf-imm-immcreatecontext) erstellen. Um den Kontext einem Fenster zu zuweisen, ruft die Anwendung die [**ImmAssociateContext-Funktion**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) auf. Diese Funktion gibt ein Handle an den zuvor zugeordneten Eingabekontext zurück. Wenn die Anwendung dem Fenster noch keinen Eingabekontext zugeordnet hat, gilt das zurückgegebene Handle für den Standardeingabekontext. In der Regel speichert die Anwendung dieses Handle und stellt es später dem Fenster neu zu, wenn der benutzerdefinierte Eingabekontext nicht mehr benötigt wird.

Sobald ein Eingabekontext einem Fenster zugeordnet ist, wählt das Betriebssystem diesen Kontext automatisch aus, wenn das Fenster aktiviert ist, und erhält den Eingabefokus. Der Stil und andere Informationen im Eingabekontext wirken sich auf nachfolgende Tastatureingaben für dieses Fenster aus und bestimmen, wie der IME funktioniert.

Ihre Anwendung muss jeden benutzerdefinierten Eingabekontext zerstören, bevor sie beendet wird. Zunächst entfernt die Anwendung den Eingabekontext aus jeder Zuordnung, die sie mit Fenstern im Thread mithilfe der [**ImmAssociateContext-Funktion vorgenommen**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) hat. Anschließend wird die [**ImmDestroyContext-Funktion**](/windows/desktop/api/Imm/nf-imm-immdestroycontext) aufgerufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Eingabemethode-Manager](about-input-method-manager.md)
</dt> </dl>

 

 



