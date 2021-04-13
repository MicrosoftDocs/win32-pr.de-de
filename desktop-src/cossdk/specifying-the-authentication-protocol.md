---
description: Angeben des Authentifizierungs Protokolls
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: Angeben des Authentifizierungs Protokolls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9bb2ec20df1ec398f32f3a1ee17334c10d9735
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483422"
---
# <a name="specifying-the-authentication-protocol"></a>Angeben des Authentifizierungs Protokolls

Abhängig von den Sicherheitsanforderungen an Ihrem Standort können Sie verlangen, dass der Dienst für Warteschlangen Dienste immer die Identität eines Clients überprüft, niemals die Identität eines Clients überprüft oder die Identität eines Clients nur dann überprüft, wenn die Komponente so konfiguriert ist, dass eine Authentifizierung erforderlich ist, auch wenn nicht über eine Warteschlange darauf zugegriffen wird.

> [!Note]  
> Um eine in der Warteschlange befindliche Komponente im Arbeitsgruppen Modus zu verwenden, muss die Authentifizierungs Ebene auf keine festgelegt werden.

 

## <a name="component-services-administrative-tool"></a>Verwaltungs Tool für Komponenten Dienste

Um das Authentifizierungsprotokoll anzugeben, führen Sie die folgenden Schritte aus:

1.  Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste unter **Komponenten Dienste** den Ordner **com+-Anwendungen** , der dem Computer zugeordnet ist, den Sie verwalten möchten.

2.  Klicken Sie mit der rechten Maustaste auf die Anwendung in der Warteschlange, für die Sie das Authentifizierungsprotokoll angeben möchten, und klicken Sie dann auf **Eigenschaften**.

3.  Wählen Sie **im Dialog** Feldeigenschaften die Registerkarte Queue aus.

4.  Wählen Sie unter **MSMQ-Nachrichten Authentifizierung** das Optionsfeld aus, das dem Authentifizierungsprotokoll zugeordnet ist, das Sie implementieren möchten.

5.  Klicken Sie auf **OK**.

## <a name="visual-basic"></a>Visual Basic

Verwenden Sie den *AUTHLEVEL* -Parameter, wenn Sie die Anwendung in der Warteschlange aktivieren, wie im [Warteschlangen-Moniker](using-the-queue-moniker.md)beschrieben.

## <a name="cc"></a>C/C++

Verwenden Sie den *AUTHLEVEL* -Parameter, wenn Sie die Anwendung in der Warteschlange aktivieren, wie im [Warteschlangen-Moniker](using-the-queue-moniker.md)beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in der Warteschlange befindliche Komponenten](queued-components-security.md)
</dt> <dt>

[Sicherheitseinschränkungen im Arbeitsgruppen Modus](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



