---
title: Player. VERSIONINFO
description: Die VERSIONINFO-Eigenschaft ruft einen Zeichen folgen Wert ab, der die Version des Windows-Media Player angibt.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- Player. VERSIONINFO-Fenster Media Player
topic_type:
- apiref
api_name:
- Player.versionInfo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44a94fa2df6d5e7d46108ec971fd84481688eb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364907"
---
# <a name="playerversioninfo"></a><span data-ttu-id="b554f-104">Player. VERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="b554f-104">Player.versionInfo</span></span>

<span data-ttu-id="b554f-105">Die **VERSIONINFO** -Eigenschaft ruft einen Zeichen folgen Wert ab, der die Version des Windows-Media Player angibt.</span><span class="sxs-lookup"><span data-stu-id="b554f-105">The **versionInfo** property retrieves a String value specifying the version of the Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="b554f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b554f-106">Syntax</span></span>

<span data-ttu-id="b554f-107">*Player* . **VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="b554f-107">*player* .**versionInfo**</span></span>

## <a name="possible-values"></a><span data-ttu-id="b554f-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="b554f-108">Possible Values</span></span>

<span data-ttu-id="b554f-109">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge** im folgenden Format: "*X*. 0,0. *Yyyy*"Where *X* steht für die Hauptversionsnummer und *yyyy* für die Buildnummer.</span><span class="sxs-lookup"><span data-stu-id="b554f-109">This property is a read-only **String** in the following format: "*X*.0.0.*YYYY*" where *X* represents the major version number and *YYYY* represents the build number.</span></span>

## <a name="examples"></a><span data-ttu-id="b554f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b554f-110">Examples</span></span>

<span data-ttu-id="b554f-111">Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das, wenn darauf geklickt wird, ein Meldungs Feld mit den Versionsinformationen für Windows Media Player anzeigt.</span><span class="sxs-lookup"><span data-stu-id="b554f-111">The following example creates an HTML BUTTON element that, when clicked, displays a message box containing the version information for Windows Media Player.</span></span> <span data-ttu-id="b554f-112">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="b554f-112">The **Player** object was created with ID = "Player".</span></span>


```
<INPUT TYPE = "BUTTON"  ID = "VERSION"  VALUE = "Show Version"
    onClick = "
        /* Build the message containing the version info. */
        var message = 'Windows Media Player Version: ';
        message += '\n';
        message += Player.versionInfo;
 
        /* Display the message box. */
        alert(message);
">

```



## <a name="requirements"></a><span data-ttu-id="b554f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b554f-113">Requirements</span></span>



| <span data-ttu-id="b554f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b554f-114">Requirement</span></span> | <span data-ttu-id="b554f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b554f-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b554f-116">Version</span><span class="sxs-lookup"><span data-stu-id="b554f-116">Version</span></span><br/> | <span data-ttu-id="b554f-117">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="b554f-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b554f-118">DLL</span><span class="sxs-lookup"><span data-stu-id="b554f-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="b554f-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b554f-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b554f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b554f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b554f-121">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b554f-121">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





