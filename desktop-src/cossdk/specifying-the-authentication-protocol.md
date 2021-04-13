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
# <a name="specifying-the-authentication-protocol"></a><span data-ttu-id="28573-103">Angeben des Authentifizierungs Protokolls</span><span class="sxs-lookup"><span data-stu-id="28573-103">Specifying the Authentication Protocol</span></span>

<span data-ttu-id="28573-104">Abhängig von den Sicherheitsanforderungen an Ihrem Standort können Sie verlangen, dass der Dienst für Warteschlangen Dienste immer die Identität eines Clients überprüft, niemals die Identität eines Clients überprüft oder die Identität eines Clients nur dann überprüft, wenn die Komponente so konfiguriert ist, dass eine Authentifizierung erforderlich ist, auch wenn nicht über eine Warteschlange darauf zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="28573-104">Depending on the security requirements at your site, you can require the queued components service always to verify a client's identity, never to verify a client's identity, or to verify a client's identity only if the component is configured to require authentication even when not accessed through a queue.</span></span>

> [!Note]  
> <span data-ttu-id="28573-105">Um eine in der Warteschlange befindliche Komponente im Arbeitsgruppen Modus zu verwenden, muss die Authentifizierungs Ebene auf keine festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="28573-105">In order to use a queued component in workgroup mode, the authentication level must be set to none.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="28573-106">Verwaltungs Tool für Komponenten Dienste</span><span class="sxs-lookup"><span data-stu-id="28573-106">Component Services Administrative Tool</span></span>

<span data-ttu-id="28573-107">Um das Authentifizierungsprotokoll anzugeben, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="28573-107">To specify the authentication protocol, use the following steps:</span></span>

1.  <span data-ttu-id="28573-108">Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste unter **Komponenten Dienste** den Ordner **com+-Anwendungen** , der dem Computer zugeordnet ist, den Sie verwalten möchten.</span><span class="sxs-lookup"><span data-stu-id="28573-108">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="28573-109">Klicken Sie mit der rechten Maustaste auf die Anwendung in der Warteschlange, für die Sie das Authentifizierungsprotokoll angeben möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="28573-109">Right-click the queued application for which you want to specify the authentication protocol, and then click **Properties**.</span></span>

3.  <span data-ttu-id="28573-110">Wählen Sie **im Dialog** Feldeigenschaften die Registerkarte Queue aus.</span><span class="sxs-lookup"><span data-stu-id="28573-110">Select the **Queuing** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="28573-111">Wählen Sie unter **MSMQ-Nachrichten Authentifizierung** das Optionsfeld aus, das dem Authentifizierungsprotokoll zugeordnet ist, das Sie implementieren möchten.</span><span class="sxs-lookup"><span data-stu-id="28573-111">Under **MSMQ Message Authentication**, select the radio button associated with the authentication protocol you want to implement.</span></span>

5.  <span data-ttu-id="28573-112">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="28573-112">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="28573-113">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="28573-113">Visual Basic</span></span>

<span data-ttu-id="28573-114">Verwenden Sie den *AUTHLEVEL* -Parameter, wenn Sie die Anwendung in der Warteschlange aktivieren, wie im [Warteschlangen-Moniker](using-the-queue-moniker.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="28573-114">Use the *AuthLevel* parameter when activating the queued application as described in the [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

## <a name="cc"></a><span data-ttu-id="28573-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="28573-115">C/C++</span></span>

<span data-ttu-id="28573-116">Verwenden Sie den *AUTHLEVEL* -Parameter, wenn Sie die Anwendung in der Warteschlange aktivieren, wie im [Warteschlangen-Moniker](using-the-queue-moniker.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="28573-116">Use the *AuthLevel* parameter when activating the queued application as described in the [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28573-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28573-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28573-118">Sicherheit in der Warteschlange befindliche Komponenten</span><span class="sxs-lookup"><span data-stu-id="28573-118">Queued Components Security</span></span>](queued-components-security.md)
</dt> <dt>

[<span data-ttu-id="28573-119">Sicherheitseinschränkungen im Arbeitsgruppen Modus</span><span class="sxs-lookup"><span data-stu-id="28573-119">Security Limitations in Workgroup Mode</span></span>](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



