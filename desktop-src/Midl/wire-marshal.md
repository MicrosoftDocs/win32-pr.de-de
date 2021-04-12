---
title: wire_marshal-Attribut
description: Das Attribut \ Wire \_ Marshal \ gibt einen Datentyp an, der anstelle eines anwendungsspezifischen Datentyps (dem userm-Type) für die Übertragung verwendet wird (der Wire-Typ).
ms.assetid: 51969f2c-7390-42c4-8aa6-ba12fdb22d23
keywords:
- Wire_marshal Attribut-Mittel l
topic_type:
- apiref
api_name:
- wire_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17466648078162bc8244219f77e3ecc0dc4cb4d7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104391143"
---
# <a name="wire_marshal-attribute"></a><span data-ttu-id="36bb0-104">Wire \_ Marshal-Attribut</span><span class="sxs-lookup"><span data-stu-id="36bb0-104">wire\_marshal attribute</span></span>

<span data-ttu-id="36bb0-105">Das **\[ Wire \_ Marshal \]** -Attribut gibt einen Datentyp an, der anstelle eines anwendungsspezifischen Datentyps (dem *userm-Type*) für die Übertragung verwendet wird (der *Wire-Typ*).</span><span class="sxs-lookup"><span data-stu-id="36bb0-105">The **\[wire\_marshal\]** attribute specifies a data type that will be used for transmission (the *wire-type*) instead of an application-specific data type (the *userm-type*).</span></span>

``` syntax
typedef [wire_marshal(wire_type)] type-specifier userm-type; 
unsigned long __RPC_USER  < userm-type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm-type > __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long  __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm-type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm-type > __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm-type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm-type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a><span data-ttu-id="36bb0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="36bb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36bb0-107">*Wire-Type*</span><span class="sxs-lookup"><span data-stu-id="36bb0-107">*wire-type*</span></span> 
</dt> <dd>

<span data-ttu-id="36bb0-108">Gibt den benannten Übertragungs Datentyp an, der zwischen Client und Server tatsächlich übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="36bb0-108">Specifies the named transfer data type that is actually transferred between client and server.</span></span> <span data-ttu-id="36bb0-109">Der Typ " *Wire-Type* " muss ein Basistyp der Mitte, ein vordefinierter Typ oder ein Typbezeichner eines Typs sein, der über das Netzwerk übertragen werden kann.</span><span class="sxs-lookup"><span data-stu-id="36bb0-109">The *wire-type* must be a MIDL base type, predefined type, or a type identifier of a type that can be transmitted across the network.</span></span>

</dd> <dt>

<span data-ttu-id="36bb0-110">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="36bb0-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="36bb0-111">Der Typ, für den *userm-Type* zu einem Alias wird.</span><span class="sxs-lookup"><span data-stu-id="36bb0-111">The type for which *userm-type* will become an alias.</span></span>

</dd> <dt>

<span data-ttu-id="36bb0-112">*User m-Type*</span><span class="sxs-lookup"><span data-stu-id="36bb0-112">*userm-type*</span></span> 
</dt> <dd>

<span data-ttu-id="36bb0-113">Gibt den Bezeichner des Benutzer Datentyps an, der gemarshallt werden soll.</span><span class="sxs-lookup"><span data-stu-id="36bb0-113">Specifies the identifier of the user data type to be marshaled.</span></span> <span data-ttu-id="36bb0-114">Dies kann ein beliebiger Typ sein, wie er vom *Typspezifizierer* angegeben wird, sofern er über eine klar definierte Größe verfügt.</span><span class="sxs-lookup"><span data-stu-id="36bb0-114">It can be any type, as given by the *type-specifier*, as long as it has a well-defined size.</span></span> <span data-ttu-id="36bb0-115">Der *userm-Typ* muss nicht transaktionabel sein, muss jedoch ein Typ sein, der dem Mittelwert Compiler bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="36bb0-115">The *userm-type* need not be transmittable but must be a type known to the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="36bb0-116">*pflags*</span><span class="sxs-lookup"><span data-stu-id="36bb0-116">*pFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="36bb0-117">Gibt einen Zeiger auf ein Flagfeld an ( [**Ganzzahl ohne Vorzeichen**](unsigned.md) [**Long**](long.md)).</span><span class="sxs-lookup"><span data-stu-id="36bb0-117">Specifies a pointer to a flag field ( [**unsigned**](unsigned.md) [**long**](long.md)).</span></span> <span data-ttu-id="36bb0-118">Das höchst wertige Wort gibt die von DCE für Gleit Komma-, Big-oder Little-Endian-und Zeichen Darstellung definierten Daten darstellungenflags der NDR-Daten an.</span><span class="sxs-lookup"><span data-stu-id="36bb0-118">The high-order word specifies NDR data representation flags as defined by DCE for floating point, big- or little-endian, and character representation.</span></span> <span data-ttu-id="36bb0-119">Mit dem nieder wertigen Wort wird ein marshallingkontextflag angegeben.</span><span class="sxs-lookup"><span data-stu-id="36bb0-119">The low-order word specifies a marshaling context flag.</span></span> <span data-ttu-id="36bb0-120">Das genaue Layout der Flags wird in [der Type \_ usersize-Funktion](/windows/desktop/Rpc/the-type-usersize-function)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="36bb0-120">The exact layout of the flags is described in [The type\_UserSize Function](/windows/desktop/Rpc/the-type-usersize-function).</span></span>

</dd> <dt>

<span data-ttu-id="36bb0-121">*Startingsize*</span><span class="sxs-lookup"><span data-stu-id="36bb0-121">*StartingSize*</span></span> 
</dt> <dd>

<span data-ttu-id="36bb0-122">Gibt die aktuelle Puffergröße (Offset) vor der Größenanpassung des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="36bb0-122">Specifies the current buffer size (offset) before sizing the object.</span></span>

</dd> <dt>

<span data-ttu-id="36bb0-123">*puser \_ TypeObject*</span><span class="sxs-lookup"><span data-stu-id="36bb0-123">*pUser\_typeObject*</span></span> 
</dt> <dd>

<span data-ttu-id="36bb0-124">Gibt einen Zeiger auf ein Objekt des *userm- \_ Typs an.*</span><span class="sxs-lookup"><span data-stu-id="36bb0-124">Specifies a pointer to an object of *userm\_type.*</span></span>

</dd> <dt>

<span data-ttu-id="36bb0-125">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="36bb0-125">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="36bb0-126">Gibt den aktuellen Puffer Zeiger an.</span><span class="sxs-lookup"><span data-stu-id="36bb0-126">Specifies the current buffer pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36bb0-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36bb0-127">Remarks</span></span>

<span data-ttu-id="36bb0-128">Jeder anwendungsspezifische Datentyp, *userm-Type,* weist eine eins-zu-eins-Entsprechung mit einem *Wire-Typ* auf, der die Wire-Darstellung des Typs definiert.</span><span class="sxs-lookup"><span data-stu-id="36bb0-128">Each application-specific data type, *userm-type,* has a one-to-one correspondence with a *wire-type* that defines the wire representation of the type.</span></span> <span data-ttu-id="36bb0-129">Sie müssen Routinen bereitstellen, um die Größe der Daten für das Marshalling, das Mars Hallen und das Entsperren der Daten und das Freigeben von Arbeitsspeicher zu verkleinern.</span><span class="sxs-lookup"><span data-stu-id="36bb0-129">You must supply routines to size the data for marshaling, to marshal and unmarshal the data, and to free memory.</span></span> <span data-ttu-id="36bb0-130">Beachten Sie Folgendes: Wenn in den Daten eingebettete Typen vorhanden sind, die auch mit **\[ Wire \_ \] Marshal** oder **\[** [**User \_ Marshal**](user-marshal.md)definiert sind **\]** , müssen Sie die Wartung dieser eingebetteten Typen ebenfalls verwalten.</span><span class="sxs-lookup"><span data-stu-id="36bb0-130">Note that if there are embedded types in your data that are also defined with **\[wire\_marshal\]** or **\[**[**user\_marshal**](user-marshal.md)**\]**, you need to manage the servicing of those embedded types also.</span></span> <span data-ttu-id="36bb0-131">Weitere Informationen zu diesen Routinen finden Sie [unter dem Wire \_ Marshal-Attribut](/windows/desktop/Rpc/the-wire-marshal-attribute).</span><span class="sxs-lookup"><span data-stu-id="36bb0-131">For more information on these routines, see [The wire\_marshal Attribute](/windows/desktop/Rpc/the-wire-marshal-attribute).</span></span>

<span data-ttu-id="36bb0-132">Ihre Implementierung muss gemäß der OSF-DCE-Spezifikation den Marshalling-Regeln folgen.</span><span class="sxs-lookup"><span data-stu-id="36bb0-132">Your implementation must follow the marshalling rules according to the OSF-DCE specification.</span></span> <span data-ttu-id="36bb0-133">Details zur Syntax der NDR-Übertragung finden Sie unter [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) .</span><span class="sxs-lookup"><span data-stu-id="36bb0-133">Details about NDR transfer syntax can be found at [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm).</span></span> <span data-ttu-id="36bb0-134">Es wird nicht empfohlen, **\[ Wire \_ Marshal \]** zu verwenden, wenn Sie mit dem Wire-Protokoll nicht vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="36bb0-134">It is not recommended to use **\[wire\_marshal\]** if you are not familiar with the wire protocol.</span></span>

<span data-ttu-id="36bb0-135">Der *Wire-Type* darf kein Schnittstellen Zeiger oder ein vollständiger Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="36bb0-135">The *wire-type* cannot be an interface pointer or a full pointer.</span></span> <span data-ttu-id="36bb0-136">Der *Wire-Typ* muss eine klar definierte Arbeitsspeicher Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="36bb0-136">The *wire-type* must have a well-defined memory size.</span></span> <span data-ttu-id="36bb0-137">Ausführliche Informationen zum Mars Hallen eines bestimmten Netzwerk *Typs* finden Sie unter [Mars Hallen von Regeln für Benutzer \_ Mars Hall und Wire \_ Marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) .</span><span class="sxs-lookup"><span data-stu-id="36bb0-137">See [Marshaling Rules for user\_marshal and wire\_marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) for details on how to marshal a given *wire-type*.</span></span>

<span data-ttu-id="36bb0-138">Der *userm-Type* darf kein Schnittstellen Zeiger sein, da diese direkt gemarshallt werden können.</span><span class="sxs-lookup"><span data-stu-id="36bb0-138">The *userm-type* should not be an interface pointer because these can be marshaled directly.</span></span> <span data-ttu-id="36bb0-139">Wenn der Benutzertyp ein vollständiger Zeiger ist, müssen Sie das Aliasing selbst verwalten.</span><span class="sxs-lookup"><span data-stu-id="36bb0-139">If the user type is a full pointer, you must manage the aliasing yourself.</span></span>

<span data-ttu-id="36bb0-140">Sie können das **\[ Wire \_ Marshal \]** -Attribut nicht direkt oder indirekt mit dem Attribut "Allocation" verwenden **\[** [](allocate.md) **\]** , da die NDR-Engine nicht die Speicher Belegung für den übertragenen Typ steuert.</span><span class="sxs-lookup"><span data-stu-id="36bb0-140">You cannot use the **\[wire\_marshal\]** attribute with the **\[**[**allocate**](allocate.md)**\]** attribute, either directly or indirectly, because the NDR engine does not control memory allocation for the transmitted type.</span></span>

## <a name="examples"></a><span data-ttu-id="36bb0-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36bb0-141">Examples</span></span>

``` syntax
typedef unsigned long _FOUR_BYTE_DATA;

typedef struct _TWO_X_TWO_BYTE_DATA 
{
        unsigned short low;
        unsigned short high;
} TWO_X_TWO_BYTE_DATA;

typedef [wire_marshal(TWO_X_TWO_BYTE_DATA)] 
    _FOUR_BYTE_DATA FOUR_BYTE_DATA; 

//Marshaling functions:

// Calculate size that converted data will 
// require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as 
// TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top 
// node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul 
    );
```

## <a name="see-also"></a><span data-ttu-id="36bb0-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="36bb0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36bb0-143">**allocate**</span><span class="sxs-lookup"><span data-stu-id="36bb0-143">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="36bb0-144">Datendarstellung</span><span class="sxs-lookup"><span data-stu-id="36bb0-144">Data Representation</span></span>](/windows/desktop/Rpc/data-representation)
</dt> <dt>

[<span data-ttu-id="36bb0-145">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="36bb0-145">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="36bb0-146">**lange**</span><span class="sxs-lookup"><span data-stu-id="36bb0-146">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="36bb0-147">**Ndrgetusermarshalinfo**</span><span class="sxs-lookup"><span data-stu-id="36bb0-147">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> <dt>

[<span data-ttu-id="36bb0-148">Das Wire \_ Marshal-Attribut</span><span class="sxs-lookup"><span data-stu-id="36bb0-148">The wire\_marshal Attribute</span></span>](/windows/desktop/Rpc/the-wire-marshal-attribute)
</dt> <dt>

[<span data-ttu-id="36bb0-149">**übertragen \_ als**</span><span class="sxs-lookup"><span data-stu-id="36bb0-149">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="36bb0-150">**Ganzzahl ohne Vorzeichen**</span><span class="sxs-lookup"><span data-stu-id="36bb0-150">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="36bb0-151">**Benutzer \_ Mars Hall**</span><span class="sxs-lookup"><span data-stu-id="36bb0-151">**user\_marshal**</span></span>](user-marshal.md)
</dt> </dl>

 

 