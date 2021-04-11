---
title: user_marshal-Attribut
description: Das \_ ACF-Attribut User Marshal ordnet einen benannten lokalen Typ in der Zielsprache (User m-Type) einem Übertragungstyp (Wire-Type) zu, der zwischen Client und Server übertragen wird.
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal Attribut-Mittel l
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5326c9390362193a1be9dc06ee3a57f174474cc2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314798"
---
# <a name="user_marshal-attribute"></a><span data-ttu-id="a4533-104">Benutzer \_ Mars Hall Attribut</span><span class="sxs-lookup"><span data-stu-id="a4533-104">user\_marshal attribute</span></span>

<span data-ttu-id="a4533-105">Das ACF-Attribut **User \_ Marshal** ordnet einen benannten lokalen Typ in der Zielsprache (*User m-Type*) einem Übertragungstyp (*Wire-* Type) zu, der zwischen Client und Server übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="a4533-105">The **user\_marshal** ACF attribute associates a named local type in the target language (*userm-type*) with a transfer type (*wire-type*) that is transferred between client and server.</span></span>

``` syntax
typedef [user_marshal(userm_type)] wire-type; 
unsigned long __RPC_USER  < userm_type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm_type >  __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long __RPC_FAR *pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm_type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm_type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm_type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a><span data-ttu-id="a4533-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4533-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4533-107">*User m-Type*</span><span class="sxs-lookup"><span data-stu-id="a4533-107">*userm-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a4533-108">Gibt den Bezeichner des Benutzer Datentyps an, der gemarshallt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4533-108">Specifies the identifier of the user data type to be marshaled.</span></span> <span data-ttu-id="a4533-109">Der *userm-Typ* muss nicht transaktierbar sein und muss kein Typ sein, der dem mittlerer l-Compiler bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a4533-109">The *userm-type* need not be transmittable and need not be a type known to the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="a4533-110">*Wire-Type*</span><span class="sxs-lookup"><span data-stu-id="a4533-110">*wire-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a4533-111">Gibt den benannten Übertragungs Datentyp an, der zwischen Client und Server tatsächlich übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="a4533-111">Specifies the named transfer data type that is actually transferred between client and server.</span></span> <span data-ttu-id="a4533-112">Der Netzwerktyp muss ein Basistyp der Mitte, ein vordefinierter Typ oder ein Typbezeichner eines Typs sein, der über das Netzwerk übertragen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a4533-112">The wire type must be a MIDL base type, predefined type, or a type identifier of a type that can be transmitted across the network.</span></span>

</dd> <dt>

<span data-ttu-id="a4533-113">*pflags*</span><span class="sxs-lookup"><span data-stu-id="a4533-113">*pFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="a4533-114">Gibt einen Zeiger auf ein Flagfeld an ( [**Ganzzahl ohne Vorzeichen**](unsigned.md) [**Long**](long.md)).</span><span class="sxs-lookup"><span data-stu-id="a4533-114">Specifies a pointer to a flag field ( [**unsigned**](unsigned.md) [**long**](long.md)).</span></span> <span data-ttu-id="a4533-115">Das höchst wertige Wort gibt die von DCE für Gleit Komma-, Big-oder Little-Endian-und Zeichen Darstellung definierten Daten darstellungenflags der NDR-Daten an.</span><span class="sxs-lookup"><span data-stu-id="a4533-115">The high-order word specifies NDR data representation flags as defined by DCE for floating point, big- or little-endian, and character representation.</span></span> <span data-ttu-id="a4533-116">Mit dem nieder wertigen Wort wird ein marshallingkontextflag angegeben.</span><span class="sxs-lookup"><span data-stu-id="a4533-116">The low-order word specifies a marshaling context flag.</span></span> <span data-ttu-id="a4533-117">Das genaue Layout der Flags wird in [der Type \_ usersize-Funktion](/windows/desktop/Rpc/the-type-usersize-function)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a4533-117">The exact layout of the flags is described in [The type\_UserSize Function](/windows/desktop/Rpc/the-type-usersize-function).</span></span>

</dd> <dt>

<span data-ttu-id="a4533-118">*Startingsize*</span><span class="sxs-lookup"><span data-stu-id="a4533-118">*StartingSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a4533-119">Gibt die aktuelle Puffergröße (Offset) vor der Größenanpassung des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="a4533-119">Specifies the current buffer size (offset) before sizing the object.</span></span>

</dd> <dt>

<span data-ttu-id="a4533-120">*puser \_ TypeObject*</span><span class="sxs-lookup"><span data-stu-id="a4533-120">*pUser\_typeObject*</span></span> 
</dt> <dd>

<span data-ttu-id="a4533-121">Gibt einen Zeiger auf ein Objekt des *userm- \_ Typs* an.</span><span class="sxs-lookup"><span data-stu-id="a4533-121">Specifies a pointer to an object of *userm\_type*.</span></span>

</dd> <dt>

<span data-ttu-id="a4533-122">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="a4533-122">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a4533-123">Gibt den aktuellen Puffer Zeiger an.</span><span class="sxs-lookup"><span data-stu-id="a4533-123">Specifies the current buffer pointer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4533-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4533-124">Remarks</span></span>

<span data-ttu-id="a4533-125">Jeder benannte lokale Typ, *userm-Type*, weist eine eins-zu-eins-Entsprechung mit einem *Wire-Typ* auf, der die Wire-Darstellung des Typs definiert.</span><span class="sxs-lookup"><span data-stu-id="a4533-125">Each named local type, *userm-type*, has a one-to-one correspondence with a *wire-type* that defines the wire representation of the type.</span></span> <span data-ttu-id="a4533-126">Sie müssen Routinen bereitstellen, um die Größe der Daten für das Marshalling, das Mars Hallen und das Entsperren der Daten und das Freigeben von Arbeitsspeicher zu verkleinern.</span><span class="sxs-lookup"><span data-stu-id="a4533-126">You must supply routines to size the data for marshaling, to marshal and unmarshal the data, and to free memory.</span></span> <span data-ttu-id="a4533-127">Weitere Informationen zu diesen Routinen finden Sie [unter User \_ Marshal Attribute](/windows/desktop/Rpc/the-user-marshal-attribute).</span><span class="sxs-lookup"><span data-stu-id="a4533-127">For more information on these routines, see [The user\_marshal Attribute](/windows/desktop/Rpc/the-user-marshal-attribute).</span></span> <span data-ttu-id="a4533-128">Beachten Sie Folgendes: Wenn in den Daten eingebettete Typen vorhanden sind, die auch mit dem **Benutzer \_ Mars** Hall oder \[ dem [**\[ Wire \_ \] Marshal**](wire-marshal.md)definiert sind, müssen Sie die Wartung dieser eingebetteten Typen ebenfalls verwalten.</span><span class="sxs-lookup"><span data-stu-id="a4533-128">Note that if there are embedded types in your data that are also defined with **user\_marshal** or \[ [**\[wire\_marshal\]**](wire-marshal.md), you need to manage the servicing of those embedded types also.</span></span>

<span data-ttu-id="a4533-129">Der *Wire-Type* darf kein Schnittstellen Zeiger oder ein vollständiger Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="a4533-129">The *wire-type* cannot be an interface pointer or a full pointer.</span></span> <span data-ttu-id="a4533-130">Der *Wire-Typ* muss eine klar definierte Arbeitsspeicher Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a4533-130">The *wire-type* must have a well-defined memory size.</span></span> <span data-ttu-id="a4533-131">Ausführliche Informationen zum Mars Hallen eines bestimmten Netzwerk *Typs* finden Sie unter [Mars Hallen von Regeln für Benutzer \_ Mars Hall und Wire \_ Marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) .</span><span class="sxs-lookup"><span data-stu-id="a4533-131">See [Marshaling Rules for user\_marshal and wire\_marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) for details on how to marshal a given *wire-type*.</span></span>

<span data-ttu-id="a4533-132">Der *userm-Type* darf kein Schnittstellen Zeiger sein, da diese direkt gemarshallt werden können.</span><span class="sxs-lookup"><span data-stu-id="a4533-132">The *userm-type* should not be an interface pointer as these can be marshaled directly.</span></span> <span data-ttu-id="a4533-133">Wenn der Benutzertyp ein vollständiger Zeiger ist, müssen Sie das Aliasing selbst verwalten.</span><span class="sxs-lookup"><span data-stu-id="a4533-133">If the user type is a full pointer, you must manage the aliasing yourself.</span></span>

## <a name="examples"></a><span data-ttu-id="a4533-134">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4533-134">Examples</span></span>

``` syntax
// Marshal a long as a structure containing two shorts.

typedef unsigned long FOUR_BYTE_DATA;
typedef struct _TWO_X_TWO_BYTE_DATA 
{ 
    unsigned short low; 
    unsigned short high; 
} TWO_X_TWO_BYTE_DATA;
```

``` syntax
// ACFL file

typedef [user_marshal(FOUR_BYTE_DATA)] TWO_X_TWO_BYTE_DATA;

// Marshaling functions:

// Calculate size that converted data will require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul);
```

## <a name="see-also"></a><span data-ttu-id="a4533-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a4533-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4533-136">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="a4533-136">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="a4533-137">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="a4533-137">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="a4533-138">**lange**</span><span class="sxs-lookup"><span data-stu-id="a4533-138">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="a4533-139">**Darstellung \_ als**</span><span class="sxs-lookup"><span data-stu-id="a4533-139">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="a4533-140">**Ganzzahl ohne Vorzeichen**</span><span class="sxs-lookup"><span data-stu-id="a4533-140">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="a4533-141">Das Mars-Attribut des Benutzers \_</span><span class="sxs-lookup"><span data-stu-id="a4533-141">The user\_marshal Attribute</span></span>](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[<span data-ttu-id="a4533-142">**Wire \_ Marshal**</span><span class="sxs-lookup"><span data-stu-id="a4533-142">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="a4533-143">**Ndrgetusermarshalinfo**</span><span class="sxs-lookup"><span data-stu-id="a4533-143">**NdrGetUserMarshalInfo**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 