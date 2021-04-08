---
title: Die type_UserSize-Funktion
description: Die Type \_ usersize-Funktion ist eine Hilfsfunktion für die Attribute "\ Wire \_ Marshal \" und "\ User \_ Marshal \".
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e5936763f9fe7b3513d66ddca7db9c35dbfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730017"
---
# <a name="the-type_usersize-function"></a><span data-ttu-id="1b9cf-104">Die Type \_ usersize-Funktion</span><span class="sxs-lookup"><span data-stu-id="1b9cf-104">The type\_UserSize Function</span></span>

<span data-ttu-id="1b9cf-105">Die **<type> \_ usersize** -Funktion ist eine Hilfsfunktion für die Attribute " \[ [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) " \] und " \[ [User \_ Marshal](/windows/desktop/Midl/user-marshal) " \] .</span><span class="sxs-lookup"><span data-stu-id="1b9cf-105">The **<type>\_UserSize** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="1b9cf-106">Die Stubdateien bezeichnen diese Funktion, um die Größe des RPC-Daten Puffers für das Benutzerdaten Objekt zu verkleinern, bevor die Daten auf der Client-oder Serverseite gemarshallt werden.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-106">The stubs call this function to size the RPC data buffer for the user data object before the data is marshaled on the client or server side.</span></span> <span data-ttu-id="1b9cf-107">Die-Funktion ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="1b9cf-107">The function is defined as:</span></span>

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

<span data-ttu-id="1b9cf-108">Der <type> im Funktionsnamen bedeutet den userm-Typ, wie in der Typdefinition für den **\[ Wire \_ \] Marshal** oder den **\[ Benutzer- \_ Marshal \]** angegeben.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-108">The <type> in the function name means the userm-type, as specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="1b9cf-109">Dieser Typ kann nicht transaktierbar oder sogar – sein, wenn er mit dem Attribut " **\[ User \_ Marshal \]** " verwendet wird – unbekannt für den mittlerer l-Compiler.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute— unknown to the MIDL compiler.</span></span> <span data-ttu-id="1b9cf-110">Der Name des Wire-Typs (der über das Netzwerk übertragene Typ) wird im Funktionsprototyp nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-110">The wire type name (the name of the type transmitted across the network) is not used in the function prototype.</span></span> <span data-ttu-id="1b9cf-111">Beachten Sie jedoch, dass der Wire-Typ das Layout für die Daten definiert, wie von OSF DCE angegeben.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-111">Note, however, that the wire type defines the layout for the data as specified by OSF DCE.</span></span> <span data-ttu-id="1b9cf-112">Alle Daten müssen in das Format der Netzwerkdaten Darstellung (NDR) konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-112">All data must be converted to network data representation (NDR) format.</span></span>

<span data-ttu-id="1b9cf-113">Der *pflags* -Parameter ist ein Zeiger auf ein Feld **ohne** Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-113">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="1b9cf-114">Das obere Wort des Flags enthält die von OSF DCE für Gleit Komma-, Byte Reihenfolge und Zeichen Darstellungen definierten NDR-Formatflags.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-114">The upper word of the flag contains NDR format flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="1b9cf-115">Das untere Wort enthält ein marshallingkontextflag, wie vom com-Kanal definiert.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-115">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="1b9cf-116">Das genaue Layout der Flags innerhalb des Felds wird in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-116">The exact layout of the flags within the field is shown in the following table.</span></span>



| <span data-ttu-id="1b9cf-117">Bits</span><span class="sxs-lookup"><span data-stu-id="1b9cf-117">Bits</span></span>  | <span data-ttu-id="1b9cf-118">Flag</span><span class="sxs-lookup"><span data-stu-id="1b9cf-118">Flag</span></span>                                  | <span data-ttu-id="1b9cf-119">Wert</span><span class="sxs-lookup"><span data-stu-id="1b9cf-119">Value</span></span>                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b9cf-120">31-24</span><span class="sxs-lookup"><span data-stu-id="1b9cf-120">31-24</span></span> | <span data-ttu-id="1b9cf-121">Gleit Komma Darstellung</span><span class="sxs-lookup"><span data-stu-id="1b9cf-121">Floating-point representation</span></span>         | <span data-ttu-id="1b9cf-122">0 = IEEE 1 = VAX 2 = Cray 3 = IBM</span><span class="sxs-lookup"><span data-stu-id="1b9cf-122">0 = IEEE 1 = VAX 2 = Cray 3 = IBM</span></span>                                                         |
| <span data-ttu-id="1b9cf-123">23-20</span><span class="sxs-lookup"><span data-stu-id="1b9cf-123">23-20</span></span> | <span data-ttu-id="1b9cf-124">Ganzzahl und Gleit Komma-Byte Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="1b9cf-124">Integer and floating-point byte order</span></span> | <span data-ttu-id="1b9cf-125">0 = Big-d 1 = Little----------</span><span class="sxs-lookup"><span data-stu-id="1b9cf-125">0 = Big-endian 1 = Little-endian</span></span>                                                          |
| <span data-ttu-id="1b9cf-126">19-16</span><span class="sxs-lookup"><span data-stu-id="1b9cf-126">19-16</span></span> | <span data-ttu-id="1b9cf-127">Zeichen Darstellung</span><span class="sxs-lookup"><span data-stu-id="1b9cf-127">Character representation</span></span>              | <span data-ttu-id="1b9cf-128">0 = ASCII 1 = EBCDIC</span><span class="sxs-lookup"><span data-stu-id="1b9cf-128">0 = ASCII 1 = EBCDIC</span></span>                                                                      |
| <span data-ttu-id="1b9cf-129">15-0</span><span class="sxs-lookup"><span data-stu-id="1b9cf-129">15-0</span></span>  | <span data-ttu-id="1b9cf-130">Marshalling von Context-Flag</span><span class="sxs-lookup"><span data-stu-id="1b9cf-130">Marshaling context flag</span></span>               | <span data-ttu-id="1b9cf-131">0 = mshctx \_ Local 1 = mshctx \_ nosharedmem 2 = mshctx \_ differenentmachine 3 = mshctx \_ INPROC</span><span class="sxs-lookup"><span data-stu-id="1b9cf-131">0 = MSHCTX\_LOCAL 1 = MSHCTX\_NOSHAREDMEM 2 = MSHCTX\_DIFFERENTMACHINE 3 = MSHCTX\_INPROC</span></span> |



 

<span data-ttu-id="1b9cf-132">Das marshallingkontextflag ermöglicht es, das Verhalten der Routine abhängig vom Kontext des RPC-Aufrufs zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-132">The marshaling context flag makes it possible to alter the behavior of your routine depending on the context for the RPC call.</span></span> <span data-ttu-id="1b9cf-133">Wenn Sie z. b. über ein Handle (**Long**) für einen Datenblock verfügen, können Sie das Handle für einen Prozess internen-Rückruf senden, aber Sie würden die eigentlichen Daten für einen-Rückruf an einen anderen Computer senden.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-133">For example, if you have a handle (**long**) to a block of data, you could send the handle for an in-process call, but you would send the actual data for a call to a different machine.</span></span> <span data-ttu-id="1b9cf-134">Das marshallingkontextflag und seine Werte werden in den Wtypes. h-und Wtypes. IDL-Dateien im Platform Software Development Kit (SDK) definiert.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-134">The marshaling context flag and its values are defined in the Wtypes.h and Wtypes.idl files in the Platform Software Development Kit (SDK).</span></span>

> [!Note]  
> <span data-ttu-id="1b9cf-135">Wenn der Wire-Typ ordnungsgemäß definiert ist, müssen Sie die Format-Flags für den NDR nicht verwenden, da die NDR-Engine die erforderlichen Konvertierungen ausführt.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-135">When the wire type is properly defined, you do not have to use the NDR format flags, as the NDR engine performs the necessary conversions.</span></span>

 

<span data-ttu-id="1b9cf-136">Der *startingsize* -Parameter ist der aktuelle Puffer Offset.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-136">The *StartingSize* a parameter is the current buffer offset.</span></span> <span data-ttu-id="1b9cf-137">Die Anfangs Größe gibt den Puffer Offset für das Benutzerobjekt an und kann möglicherweise nicht ordnungsgemäß ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-137">The starting size indicates the buffer offset for the user object, and it may or may not be aligned properly.</span></span> <span data-ttu-id="1b9cf-138">Ihre Routine muss alle erforderlichen Auffüll Zeichen berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-138">Your routine should account for whatever padding is necessary.</span></span>

<span data-ttu-id="1b9cf-139">Der *pmyobj* -Parameter ist ein Zeiger auf ein Benutzertyp Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-139">The *pMyObj* parameter is a pointer to a user type object.</span></span>

<span data-ttu-id="1b9cf-140">Der Rückgabewert ist die neue Offset-oder Puffer Position.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-140">The return value is the new offset or buffer position.</span></span> <span data-ttu-id="1b9cf-141">Die-Funktion sollte die kumulative Größe zurückgeben. dabei handelt es sich um die Anfangs Größe Plus mögliche Auffüll Zeichen zuzüglich der Datengröße.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-141">The function should return the cumulative size, which is the starting size plus possible padding plus the data size.</span></span>

<span data-ttu-id="1b9cf-142">Die **<type> \_ usersize** -Funktion kann eine Überschätzung der benötigten Größe zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-142">The **<type>\_UserSize** function can return an overestimate of the size needed.</span></span> <span data-ttu-id="1b9cf-143">Die tatsächliche Größe des gesendeten Puffers wird durch die Datengröße, nicht durch die Puffer Zuordnungs Größe definiert.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-143">The actual size of the sent buffer is defined by the data size, not by the buffer allocation size.</span></span>

<span data-ttu-id="1b9cf-144">Die **<type> \_ usersize** -Funktion wird nicht aufgerufen, wenn die Wire-Größe zur Kompilierzeit berechnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-144">The **<type>\_UserSize** function is not called if the wire size can be computed at compile time.</span></span> <span data-ttu-id="1b9cf-145">Beachten Sie, dass die tatsächliche Größe der Wire-Darstellung bei den meisten Unions nur zur Laufzeit bestimmt werden kann, auch wenn keine Zeiger vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="1b9cf-145">Note that for most unions, even if there are no pointers, the actual size of the wire representation can be determined only at run time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b9cf-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1b9cf-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b9cf-147">Marshalling von Regeln für das Mars Hallen von Benutzern und das übertragen \_ \_</span><span class="sxs-lookup"><span data-stu-id="1b9cf-147">Marshaling rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="1b9cf-148">Benutzer \_ Mars Hall</span><span class="sxs-lookup"><span data-stu-id="1b9cf-148">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="1b9cf-149">Wire \_ Marshal</span><span class="sxs-lookup"><span data-stu-id="1b9cf-149">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 