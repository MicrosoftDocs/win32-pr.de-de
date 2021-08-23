---
description: Angeben des Authentifizierungsprotokolls
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: Angeben des Authentifizierungsprotokolls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c4688894543a45f49c4af470658da97e30a159c47025398ac7c7ae5e0620e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610510"
---
# <a name="specifying-the-authentication-protocol"></a>Angeben des Authentifizierungsprotokolls

Abhängig von den Sicherheitsanforderungen an Ihrem Standort können Sie festlegen, dass der Dienst mit den komponenten in der Warteschlange immer die Identität eines Clients, nie die Identität eines Clients oder die Identität eines Clients nur dann überprüft, wenn die Komponente so konfiguriert ist, dass sie eine Authentifizierung erfordert, auch wenn nicht über eine Warteschlange darauf zugegriffen wird.

> [!Note]  
> Um eine Komponente in der Warteschlange im Arbeitsgruppenmodus zu verwenden, muss die Authentifizierungsebene auf "None" festgelegt werden.

 

## <a name="component-services-administrative-tool"></a>Verwaltungstool "Komponentendienste"

Um das Authentifizierungsprotokoll anzugeben, verwenden Sie die folgenden Schritte:

1.  Öffnen Sie in der Konsolenstruktur des Component Services-Verwaltungstools unter **Komponentendienste** den Ordner **COM+-Anwendungen,** der dem Computer zugeordnet ist, den Sie verwalten möchten.

2.  Klicken Sie mit der rechten Maustaste auf die Anwendung in der Warteschlange, für die Sie das Authentifizierungsprotokoll angeben möchten, und klicken Sie dann auf **Eigenschaften.**

3.  Wählen Sie im Eigenschaftendialogfeld die Registerkarte **Queuing** aus.

4.  Wählen Sie unter **MSMQ-Nachrichtenauthentifizierung** das Optionsfeld aus, das dem Authentifizierungsprotokoll zugeordnet ist, das Sie implementieren möchten.

5.  Klicken Sie auf **OK**.

## <a name="visual-basic"></a>Visual Basic

Verwenden Sie den *AuthLevel-Parameter,* wenn Sie die Anwendung in der Warteschlange aktivieren, wie unter Verwenden des [Warteschlangenmonikers](using-the-queue-moniker.md)beschrieben.

## <a name="cc"></a>C/C++

Verwenden Sie den *AuthLevel-Parameter,* wenn Sie die Anwendung in der Warteschlange aktivieren, wie unter Verwenden des [Warteschlangenmonikers](using-the-queue-moniker.md)beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit von Komponenten in der Warteschlange](queued-components-security.md)
</dt> <dt>

[Sicherheitseinschränkungen im Arbeitsgruppenmodus](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



