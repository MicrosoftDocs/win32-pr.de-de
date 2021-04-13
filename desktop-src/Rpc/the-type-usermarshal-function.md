---
title: Die type_UserMarshal-Funktion
description: Die Type \_ usermarshal-Funktion ist eine Hilfsfunktion für die Attribute "\ Wire \_ Marshal \" und "\ User \_ Marshal \".
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca4cc8ced4b84e21475960912f8e4ac2054d1c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390977"
---
# <a name="the-type_usermarshal-function"></a><span data-ttu-id="efc23-104">Der Typ \_ usermarshal-Funktion</span><span class="sxs-lookup"><span data-stu-id="efc23-104">The type\_UserMarshal Function</span></span>

<span data-ttu-id="efc23-105">Die **<type> \_ usermarshal** -Funktion ist eine Hilfsfunktion für die Attribute " \[ [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) " \] und " \[ [User \_ Marshal](/windows/desktop/Midl/user-marshal) " \] .</span><span class="sxs-lookup"><span data-stu-id="efc23-105">The **<type>\_UserMarshal** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="efc23-106">Diese Funktion wird von den Stubdaten aufgerufen, um Daten auf der Client-oder Serverseite zu Mars Hallen.</span><span class="sxs-lookup"><span data-stu-id="efc23-106">The stubs call this function to marshal data on the client or server side.</span></span> <span data-ttu-id="efc23-107">Die-Funktion ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="efc23-107">The function is defined as:</span></span>

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<span data-ttu-id="efc23-108">Der <type> im Funktionsnamen bedeutet, dass der userm-Typ in der Typdefinition für den **\[ Wire \_ Marshal \]** oder den **\[ Benutzer- \_ Marshal \]** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="efc23-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="efc23-109">Dieser Typ ist möglicherweise nicht transaktierbar oder sogar – bei Verwendung mit dem Attribut " **\[ User \_ Marshal \]** " – ein Typ, der dem Mittelwert Compiler unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="efc23-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute—a type unknown to the MIDL compiler.</span></span> <span data-ttu-id="efc23-110">Der Name des Wire-Typs (der Name des übertragbaren Typs) wird im Funktionsprototyp nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="efc23-110">The wire type name (the name of transmissible type) is not used in the function prototype.</span></span> <span data-ttu-id="efc23-111">Beachten Sie jedoch, dass der Wire-Typ das von OSF DCE angegebene Netzwerk Layout für die Daten definiert.</span><span class="sxs-lookup"><span data-stu-id="efc23-111">Note, however, that the wire type defines the wire layout for the data as specified by OSF DCE.</span></span>

<span data-ttu-id="efc23-112">Der *pflags* -Parameter ist ein Zeiger auf ein Feld ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="efc23-112">The *pFlags* parameter is a pointer to an unsigned long flag field.</span></span> <span data-ttu-id="efc23-113">Das obere Wort des Flags enthält von OSF-DCE für Gleit Komma-, Byte Reihenfolge-und Zeichen Darstellungen definierte Daten der Datendarstellung von NDR-Daten.</span><span class="sxs-lookup"><span data-stu-id="efc23-113">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="efc23-114">Das untere Wort enthält ein marshallingkontextflag, wie vom com-Kanal definiert.</span><span class="sxs-lookup"><span data-stu-id="efc23-114">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="efc23-115">Das genaue Layout der Flags innerhalb des Felds wird in [der Type \_ usersize-Funktion](the-type-usersize-function.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="efc23-115">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="efc23-116">Der *pbuffer* -Parameter ist der aktuelle Puffer Zeiger.</span><span class="sxs-lookup"><span data-stu-id="efc23-116">The *pBuffer* parameter is the current buffer pointer.</span></span> <span data-ttu-id="efc23-117">Dieser Zeiger kann beim Eintrag nicht ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="efc23-117">This pointer may or may not be aligned on entry.</span></span> <span data-ttu-id="efc23-118">Die **<type> \_ usermarshal** -Funktion sollte den Puffer Zeiger entsprechend ausrichten, die Daten Mars Hallen und die neue Puffer Position zurückgeben. dabei handelt es sich um die Adresse des ersten Bytes nach dem gemarshallten Objekt.</span><span class="sxs-lookup"><span data-stu-id="efc23-118">Your **<type>\_UserMarshal** function should align the buffer pointer appropriately, marshal the data, and return the new buffer position, which is the address of the first byte after the marshaled object.</span></span> <span data-ttu-id="efc23-119">Beachten Sie, dass die Wire Type-Spezifikation das tatsächliche Layout der Daten im Puffer bestimmt.</span><span class="sxs-lookup"><span data-stu-id="efc23-119">Keep in mind that the wire type specification determines the actual layout of the data in the buffer.</span></span>

<span data-ttu-id="efc23-120">Der *pmyobj* -Parameter ist ein Zeiger auf ein Benutzertyp Objekt.</span><span class="sxs-lookup"><span data-stu-id="efc23-120">The *pMyObj* parameter is a pointer to a user type object.</span></span>

<span data-ttu-id="efc23-121">Der Rückgabewert ist die neue Puffer Position, bei der es sich um die Adresse des ersten Bytes nach dem nicht gemarshallten Objekt handelt.</span><span class="sxs-lookup"><span data-stu-id="efc23-121">The return value is the new buffer position, which is the address of the first byte after the unmarshaled object.</span></span>

<span data-ttu-id="efc23-122">Ein Pufferüberlauf kann auftreten, wenn Sie die Größe der Daten falsch berechnen und versuchen, mehr Daten als erwartet zu Mars Hallen.</span><span class="sxs-lookup"><span data-stu-id="efc23-122">Buffer overflow can occur when you incorrectly calculate the size of the data and attempt to marshal more data than expected.</span></span> <span data-ttu-id="efc23-123">Sie sollten darauf achten, diese Situation zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="efc23-123">You should be careful to avoid this situation.</span></span> <span data-ttu-id="efc23-124">Sie können dies überprüfen, indem Sie den Zeiger verwenden, den **<type> \_ usermarshal** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="efc23-124">You can check against it by using the pointer that **<type>\_UserMarshal** returns.</span></span> <span data-ttu-id="efc23-125">Andernfalls riskieren Sie, dass die NDR-Engine später eine Pufferüberlauf Ausnahme auslöst.</span><span class="sxs-lookup"><span data-stu-id="efc23-125">Otherwise, you risk having the NDR engine raise a buffer-overflow exception later.</span></span>

<span data-ttu-id="efc23-126">Ausnahmen müssen abgefangen und lokal behandelt werden, Ausnahmen dürfen nicht in der aufzurufenden aufrufsstapel angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="efc23-126">Exceptions must be caught and handled locally, exceptions must not be allowed to propigated up the call stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="efc23-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="efc23-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efc23-128">Marshalling von Regeln für das Mars Hallen von Benutzern und das übertragen \_ \_</span><span class="sxs-lookup"><span data-stu-id="efc23-128">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="efc23-129">Wire \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="efc23-129">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="efc23-130">Benutzer \_ Mars Hall</span><span class="sxs-lookup"><span data-stu-id="efc23-130">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 