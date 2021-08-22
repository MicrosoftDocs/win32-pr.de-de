---
description: Erzwingen der Aktivierung im Aufruferkontext
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: Erzwingen der Aktivierung im Aufruferkontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42cb657ad7d11f61de0737ca7ac935d1d570649c3e0da9db9b63c79edea38cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567420"
---
# <a name="enforcing-activation-in-the-callers-context"></a>Erzwingen der Aktivierung im Kontext des Aufrufers

Sie können steuern, ob ein Objekt in seinem eigenen Kontext aktiviert wird. Wenn Sie das Component Services-Verwaltungstool verwenden, um die Komponentenaktivierung im Kontext des Aufrufers zu er erfordern, tritt Folgendes auf, wenn COM+ eine Instanz der Komponente in einem Kontext aktiviert:

-   Das Objekt wird nach Möglichkeit im Kontext des Erstellers aktiviert.
-   Die Objektaktivierung schlägt fehl, wenn sie einen eigenen Kontext erfordert. ES \_ WIRD \_ VERSUCHT, AUßERHALB DES \_ \_ \_ \_ CLIENTKONTEXTS \_ ZU ERSTELLEN.

Ob das Objekt einen eigenen Kontext erfordert, hängt von seiner Konfiguration relativ zum aktuellen Zustand der Kontexteigenschaften des Aufrufers ab. Weitere Informationen finden Sie unter [COM+-Kontexte.](com--contexts.md)

Sie möchten die Aktivierung auf dieser Ebene steuern, wenn ein Aspekt Ihres Objekts nicht ordnungsgemäß funktioniert, wenn es über einen eigenen Kontext verfügt. Wenn die Komponente z. B. kein Marshalling unterstützt und über einen eigenen Kontext verfügt, können alle Aufrufe daran fehlschlagen, da kontextübergreifende Aufrufe abgefangen und ein schlanker Marshall ausgeführt wird.

**So erzwingen Sie die Aktivierung im Kontext des Aufrufers**

1.  Klicken Sie im Detailbereich des Verwaltungstool Komponentendienste mit der  rechten Maustaste auf die Komponente (die sich im Ordner Komponenten einer beliebigen ausgewählten COM+-Anwendung befindet), für die Sie Aktivierungseigenschaften festlegen, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die **Registerkarte Aktivierung.**

3.  Aktivieren Sie das Kontrollkästchen Muss **im Kontext der Aufrufer** aktiviert werden.

4.  Klicken Sie auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte der COM+-Just-In-Time-Aktivierung](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Erzwingen der Aktivierung im Standardkontext](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



