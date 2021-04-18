---
description: Legt einen booleschen Wert fest, der angibt, ob Benutzeroberflächen Aufforderungen für die Identität eines Signatur Gebers oder Absenders verwendet werden können, oder ruft ihn ab.
ms.assetid: b9765de4-0b94-4006-aaa8-9ad6858da1f4
title: Settings. enablepromptforcertifiereui (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.EnablePromptForCertificateUI
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e494c98e2a828b512b0bb66dc2a44cba8c37792c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368597"
---
# <a name="settingsenablepromptforcertificateui-property"></a><span data-ttu-id="eca8c-103">Settings. enablepromptforcertifiereui (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="eca8c-103">Settings.EnablePromptForCertificateUI property</span></span>

<span data-ttu-id="eca8c-104">\[Die **enablepromptforcertifi-EUI** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]</span><span class="sxs-lookup"><span data-stu-id="eca8c-104">\[The **EnablePromptForCertificateUI** property is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="eca8c-105">Mit der **enablepromptforcertifitoreui** -Eigenschaft wird ein boolescher Wert festgelegt oder abgerufen, der angibt, ob Benutzeroberflächen Aufforderungen für die Identität eines Signatur Gebers oder Absenders verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="eca8c-105">The **EnablePromptForCertificateUI** property sets or retrieves a Boolean value that specifies whether user interface prompts for a signer or sender's identity can be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="eca8c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="eca8c-106">Syntax</span></span>


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a><span data-ttu-id="eca8c-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="eca8c-107">Property value</span></span>

<span data-ttu-id="eca8c-108">**True** gibt an, dass die Benutzeroberfläche zur Eingabe eines Signatur Gebers oder der Absender Identität verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="eca8c-108">If **true**, user interface prompts for a signer or sender's identity can be used.</span></span> <span data-ttu-id="eca8c-109">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="eca8c-109">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="eca8c-110">Wenn Sie diese Eigenschaft festlegen, werden Warnungen nicht deaktiviert, die generiert werden, bevor die Verwendung von privaten Schlüsseln aus einer webbasierten Anwendung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="eca8c-110">Setting this property does not disable warnings that are generated before any private key usage is done from a web-based application.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eca8c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eca8c-111">Requirements</span></span>



| <span data-ttu-id="eca8c-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eca8c-112">Requirement</span></span> | <span data-ttu-id="eca8c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="eca8c-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eca8c-114">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="eca8c-114">Redistributable</span></span><br/> | <span data-ttu-id="eca8c-115">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="eca8c-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="eca8c-116">DLL</span><span class="sxs-lookup"><span data-stu-id="eca8c-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="eca8c-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eca8c-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eca8c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eca8c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eca8c-119">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="eca8c-119">**Settings**</span></span>](settings.md)
</dt> </dl>

 

 




