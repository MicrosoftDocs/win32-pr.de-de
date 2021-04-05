---
title: HelpFile (Eigenschaft)
description: HelpFile (Eigenschaft)
ms.assetid: 18a5fd9b-4ca7-4701-9993-1e0c55f6e232
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d5307abfba0f884261f5b4a21131a75cf87224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710920"
---
# <a name="helpfile-property"></a><span data-ttu-id="0d2f6-103">HelpFile (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0d2f6-103">HelpFile Property</span></span>

<span data-ttu-id="0d2f6-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0d2f6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0d2f6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d2f6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0d2f6-106">Gibt den Pfad und den Dateinamen für eine kontextabhängige Microsoft Windows-Hilfedatei zurück, die von der Client Anwendung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-106">Returns or sets the path and filename for a Microsoft Windows context-sensitive Help file supplied by the client application.</span></span>

</dd> <dt>

<span data-ttu-id="0d2f6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="0d2f6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0d2f6-108">\*Agent. ***Zeichen ("*** Merkmal-ID \* \* *"). HelpFile* \*  \[  =  *Dateiname*\]</span><span class="sxs-lookup"><span data-stu-id="0d2f6-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Helpfile** \[ = *Filename*\]</span></span>



| <span data-ttu-id="0d2f6-109">Teil</span><span class="sxs-lookup"><span data-stu-id="0d2f6-109">Part</span></span>       | <span data-ttu-id="0d2f6-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d2f6-110">Description</span></span>                                                                    |
|------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0d2f6-111">*Filename*</span><span class="sxs-lookup"><span data-stu-id="0d2f6-111">*Filename*</span></span> | <span data-ttu-id="0d2f6-112">Ein Zeichen folgen Ausdruck, der den Pfad und den Dateinamen der Windows-Hilfedatei angibt.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-112">A string expression specifying the path and filename of the Windows Help file.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d2f6-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d2f6-113">Remarks</span></span>

<span data-ttu-id="0d2f6-114">Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die **HelpFile** -Eigenschaft des Zeichens festgelegt haben, ruft der-Agent automatisch die Hilfe auf, wenn [**helpmadeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer auf das Zeichen klickt oder einen Befehl aus dem Popupmenü auswählt.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-114">If you've created a Windows Help file for your application and set the character's **HelpFile** property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="0d2f6-115">Wenn Sie in der [**HelpContextID**](helpcontextid-property.md) -Eigenschaft des ausgewählten Befehls eine Kontext Nummer angegeben haben, wird in der Hilfe ein Thema angezeigt, das dem aktuellen Hilfe Kontext entspricht. Andernfalls wird "kein Hilfethema mit diesem Element verknüpft" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-115">If you specified a context number in the [**HelpContextID**](helpcontextid-property.md) property of the selected command, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="0d2f6-116">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d2f6-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0d2f6-117">See Also</span></span>

<span data-ttu-id="0d2f6-118">[**Helpmudeon-Eigenschaft**](helpmodeon-property.md), [ **HelpContextID-Eigenschaft**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="0d2f6-118">[**HelpModeOn property**](helpmodeon-property.md), [**HelpContextID property**](helpcontextid-property.md)</span></span>


 

 




