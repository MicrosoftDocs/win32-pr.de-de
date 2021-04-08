---
title: HelpContextID-Eigenschaft (Befehls Objekt)
description: HelpContextID (Eigenschaft)
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef0fcfb24aee7aed75f8eb794e81291207ea24
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102754"
---
# <a name="helpcontextid-property-command-object"></a><span data-ttu-id="3ec68-103">HelpContextID-Eigenschaft (Befehls Objekt)</span><span class="sxs-lookup"><span data-stu-id="3ec68-103">HelpContextID Property (Command Object)</span></span>

<span data-ttu-id="3ec68-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3ec68-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3ec68-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ec68-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3ec68-106">Gibt eine zugeordnete Kontext Nummer für das [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="3ec68-106">Returns or sets an associated context number for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="3ec68-107">Wird verwendet, um kontextbezogene Hilfe für das **Befehls** Objekt bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3ec68-107">Used to provide context-sensitive Help for the **Command** object.</span></span>

</dd> <dt>

<span data-ttu-id="3ec68-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="3ec68-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3ec68-109">\*Agent. *-**Zeichen ("**_Merkmal-ID_*_"). Befehle (""). HelpContextID_- \*  \[  =  *Nummer*\]</span><span class="sxs-lookup"><span data-stu-id="3ec68-109">*agent.\***Characters("**_CharacterID_*_").Commands("").HelpContextID_\* \[ = *Number*\]</span></span>



| <span data-ttu-id="3ec68-110">Teil</span><span class="sxs-lookup"><span data-stu-id="3ec68-110">Part</span></span>     | <span data-ttu-id="3ec68-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ec68-111">Description</span></span>                                   |
|----------|-----------------------------------------------|
| <span data-ttu-id="3ec68-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="3ec68-112">*Number*</span></span> | <span data-ttu-id="3ec68-113">Eine ganze Zahl, die eine gültige Kontext Nummer angibt.</span><span class="sxs-lookup"><span data-stu-id="3ec68-113">An integer specifying a valid context number.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ec68-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ec68-114">Remarks</span></span>

<span data-ttu-id="3ec68-115">Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens auf die Datei festgelegt haben, ruft der-Agent automatisch die Hilfe auf, wenn [**helpmudeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer den Befehl auswählt.</span><span class="sxs-lookup"><span data-stu-id="3ec68-115">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property to the file, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="3ec68-116">Wenn Sie in [**HelpContextID**](helpcontextid-property.md)eine Kontext Nummer festlegen, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontext Nummer identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="3ec68-116">If you set a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="3ec68-117">Die aktuelle Kontext Nummer ist der Wert von **HelpContextID** für den Befehl.</span><span class="sxs-lookup"><span data-stu-id="3ec68-117">The current context number is the value of **HelpContextID** for the command.</span></span>

<span data-ttu-id="3ec68-118">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="3ec68-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="3ec68-119">Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.</span><span class="sxs-lookup"><span data-stu-id="3ec68-119">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="3ec68-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3ec68-120">See Also</span></span>

[<span data-ttu-id="3ec68-121">**HelpFile (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="3ec68-121">**HelpFile property**</span></span>](helpfile-property.md)


 

 
