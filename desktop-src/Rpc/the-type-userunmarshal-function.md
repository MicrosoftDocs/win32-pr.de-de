---
title: Die type_UserUnmarshal-Funktion
description: Der Typ \_ userunmarshal-Funktion ist eine Hilfsfunktion für die Attribute "\ Wire \_ Marshal \" und "\ User \_ Marshal \".
ms.assetid: ee7a0e96-11ec-4d15-9d4b-55cc175fdd55
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332edbc2391aadf297789cc0ae862454786bdd8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039565"
---
# <a name="the-type_userunmarshal-function"></a><span data-ttu-id="19fe7-104">Der Typ \_ userunmarshal-Funktion</span><span class="sxs-lookup"><span data-stu-id="19fe7-104">The type\_UserUnmarshal Function</span></span>

<span data-ttu-id="19fe7-105">Die **<type> \_ userunmarshal** -Funktion ist eine Hilfsfunktion für das \[ [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) \] -Attribut und das \[ [User \_ Marshal](/windows/desktop/Midl/user-marshal) - \] Attribut.</span><span class="sxs-lookup"><span data-stu-id="19fe7-105">The **<type>\_UserUnmarshal** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="19fe7-106">Diese Funktion wird von den Stubdateien aufgerufen, um die Daten auf Client-oder Serverseite zu Mars Hallen.</span><span class="sxs-lookup"><span data-stu-id="19fe7-106">The stubs call this function to unmarshal data on the client or server side.</span></span> <span data-ttu-id="19fe7-107">Die-Funktion ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="19fe7-107">The function is defined as:</span></span>

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserUnmarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<span data-ttu-id="19fe7-108">Der <type> im Funktionsnamen bedeutet, dass der userm-Typ in der Typdefinition für den **\[ Wire \_ Marshal \]** oder den **\[ Benutzer- \_ Marshal \]** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="19fe7-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="19fe7-109">Dieser Typ kann nicht transaktierbar oder sogar – sein, wenn er mit dem Attribut " **\[ User \_ Marshal \]** " verwendet wird – unbekannt für den mittlerer l-Compiler.</span><span class="sxs-lookup"><span data-stu-id="19fe7-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute—unknown to the MIDL compiler.</span></span> <span data-ttu-id="19fe7-110">Der Name des Wire-Typs (der Name des übertragbaren Typs) wird im Funktionsprototyp nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="19fe7-110">The wire type name (the name of transmissible type) is not used in the function prototype.</span></span> <span data-ttu-id="19fe7-111">Beachten Sie jedoch, dass der Wire-Typ das von OSF DCE angegebene Netzwerk Layout für die Daten definiert.</span><span class="sxs-lookup"><span data-stu-id="19fe7-111">Note, however, that the wire type defines the wire layout for the data as specified by OSF DCE.</span></span>

<span data-ttu-id="19fe7-112">Der *pflags* -Parameter ist ein Zeiger auf ein Feld **ohne** Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="19fe7-112">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="19fe7-113">Das obere Wort des Flags enthält von OSF-DCE für Gleit Komma-, Byte Reihenfolge-und Zeichen Darstellungen definierte Daten der Datendarstellung von NDR-Daten.</span><span class="sxs-lookup"><span data-stu-id="19fe7-113">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="19fe7-114">Das untere Wort enthält ein marshallingkontextflag, wie vom com-Kanal definiert.</span><span class="sxs-lookup"><span data-stu-id="19fe7-114">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="19fe7-115">Das genaue Layout der Flags innerhalb des Felds wird in [der Type \_ usersize-Funktion](the-type-usersize-function.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="19fe7-115">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="19fe7-116">Der *pbuffer* -Parameter ist der aktuelle Puffer Zeiger.</span><span class="sxs-lookup"><span data-stu-id="19fe7-116">The *pBuffer* parameter is the current buffer pointer.</span></span> <span data-ttu-id="19fe7-117">Dieser Zeiger kann beim Eintrag nicht ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="19fe7-117">This pointer may or may not be aligned on entry.</span></span> <span data-ttu-id="19fe7-118">Ihre **<type> \_ userunmarshal** -Funktion sollte den Puffer Zeiger entsprechend ausrichten, das Mars Hallen der Daten rückgängig macht und die neue Puffer Position zurückgeben. Dies ist die Adresse des ersten Bytes nach dem nicht gemarshallten Objekt.</span><span class="sxs-lookup"><span data-stu-id="19fe7-118">Your **<type>\_UserUnmarshal** function should align the buffer pointer appropriately, unmarshal the data, and return the new buffer position, which is the address of the first byte after the unmarshaled object.</span></span>

<span data-ttu-id="19fe7-119">Der *pmyobj* -Parameter ist ein Zeiger auf ein benutzerdefiniertes Typobjekt.</span><span class="sxs-lookup"><span data-stu-id="19fe7-119">The *pMyObj* parameter is a pointer to a user-defined type object.</span></span>

<span data-ttu-id="19fe7-120">In einer heterogenen Umgebung führt die NDR-Engine jede erforderliche Datenkonvertierung aus, bevor die **<type> \_ userunmarshal** -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="19fe7-120">In a heterogeneous environment, the NDR engine performs any data conversion necessary before calling the **<type>\_UserUnmarshal** function.</span></span> <span data-ttu-id="19fe7-121">Beachten Sie, dass die NDR-Engine diese Datenkonvertierung gemäß der für diesen Benutzer Datentyp angegebenen Typdefinition ausführt.</span><span class="sxs-lookup"><span data-stu-id="19fe7-121">Note that the NDR engine carries out this data conversion according to the wire-type definition supplied for this user data type.</span></span> <span data-ttu-id="19fe7-122">Das-Flag gibt die Datendarstellung des Absenders an.</span><span class="sxs-lookup"><span data-stu-id="19fe7-122">The flag indicates the data representation of the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19fe7-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19fe7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19fe7-124">Marshalling von Regeln für das Mars Hallen von Benutzern und das übertragen \_ \_</span><span class="sxs-lookup"><span data-stu-id="19fe7-124">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="19fe7-125">Wire \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="19fe7-125">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="19fe7-126">Benutzer \_ Mars Hall</span><span class="sxs-lookup"><span data-stu-id="19fe7-126">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 