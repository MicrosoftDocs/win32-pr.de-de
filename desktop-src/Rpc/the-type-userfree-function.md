---
title: Die type_UserFree-Funktion
description: Die Type \_ userfree-Funktion ist eine Hilfsfunktion für die Attribute "\ Wire \_ Marshal \" und "\ User \_ Marshal \".
ms.assetid: cc83a074-ea6c-432a-92fe-6397a6dc3c3c
keywords:
- type_UserFree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e923388b37a39a325c0868deca7e7926a3d7705
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727441"
---
# <a name="the-type_userfree-function"></a><span data-ttu-id="47fd4-104">Die Type \_ userfree-Funktion</span><span class="sxs-lookup"><span data-stu-id="47fd4-104">The type\_UserFree Function</span></span>

<span data-ttu-id="47fd4-105">Die **<type> \_ userfree** -Funktion ist eine Hilfsfunktion für die Attribute " \[ [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) " \] und " \[ [User \_ Marshal](/windows/desktop/Midl/user-marshal) " \] .</span><span class="sxs-lookup"><span data-stu-id="47fd4-105">The **<type>\_UserFree** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="47fd4-106">Diese Funktion wird von den Stubdateien aufgerufen, um die Daten auf der Serverseite freizugeben.</span><span class="sxs-lookup"><span data-stu-id="47fd4-106">The stubs call this function to free the data on the server side.</span></span> <span data-ttu-id="47fd4-107">Die-Funktion ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="47fd4-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER  <type>_UserFree(
    unsigned long __RPC_FAR * pFlags,
    <type_name>  __RPC_FAR *  pMyObj );
```

<span data-ttu-id="47fd4-108">Der <type> im Funktionsnamen bedeutet, dass der userm-Typ in der Typdefinition für den **\[ Wire \_ Marshal \]** oder den **\[ Benutzer- \_ Marshal \]** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="47fd4-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span>

<span data-ttu-id="47fd4-109">Der *pflags* -Parameter ist ein Zeiger auf ein Feld **ohne** Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="47fd4-109">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="47fd4-110">Das obere Wort des Flags enthält von OSF-DCE für Gleit Komma-, Byte Reihenfolge-und Zeichen Darstellungen definierte Daten der Datendarstellung von NDR-Daten.</span><span class="sxs-lookup"><span data-stu-id="47fd4-110">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="47fd4-111">Das untere Wort enthält ein marshallingkontextflag, wie vom com-Kanal definiert.</span><span class="sxs-lookup"><span data-stu-id="47fd4-111">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="47fd4-112">Das genaue Layout der Flags innerhalb des Felds wird in [der Type \_ usersize-Funktion](the-type-usersize-function.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="47fd4-112">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="47fd4-113">Der *pmyobj* -Parameter ist ein Zeiger auf ein Benutzertyp Objekt.</span><span class="sxs-lookup"><span data-stu-id="47fd4-113">The *pMyObj* parameter is a pointer to a user type object.</span></span> <span data-ttu-id="47fd4-114">Die NDR-Engine gibt das Objekt der obersten Ebene frei.</span><span class="sxs-lookup"><span data-stu-id="47fd4-114">The NDR engine frees the top-level object.</span></span> <span data-ttu-id="47fd4-115">Sie sind dafür verantwortlich, alle Objekte freizugeben, auf die das Objekt der obersten Ebene verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="47fd4-115">You are responsible for freeing any objects to which the top-level object may point.</span></span>

<span data-ttu-id="47fd4-116">Ausnahmen müssen abgefangen und lokal behandelt werden, Ausnahmen dürfen nicht in der aufzurufenden aufrufsstapel angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="47fd4-116">Exceptions must be caught and handled locally, exceptions must not be allowed to propigated up the call stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47fd4-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47fd4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47fd4-118">Marshalling von Regeln für das Mars Hallen von Benutzern und das übertragen \_ \_</span><span class="sxs-lookup"><span data-stu-id="47fd4-118">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="47fd4-119">Wire \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="47fd4-119">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="47fd4-120">Benutzer \_ Mars Hall</span><span class="sxs-lookup"><span data-stu-id="47fd4-120">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 