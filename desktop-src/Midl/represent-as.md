---
title: represent_as-Attribut
description: Das Attribut \ ist \_ As \ ACF ordnet einen benannten lokalen Typ in der Zielsprache repr-Type mit einem Übertragungstyp namens-Type zu, der zwischen Client und Server übertragen wird.
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- represent_as Attribut-Mittel l
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17d0b8915e75bb3065b394ef76900bd8efb5e0c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037722"
---
# <a name="represent_as-attribute"></a><span data-ttu-id="4d884-104">\_als Attribut darstellen</span><span class="sxs-lookup"><span data-stu-id="4d884-104">represent\_as attribute</span></span>

<span data-ttu-id="4d884-105">Das Attribut " **\[ \_ As \]** ACF" wird in der Zielsprache " *repr-Type* " mit einem Übertragungstyp *namens "-Type* " verknüpft, der zwischen Client und Server übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="4d884-105">The **\[represent\_as\]** ACF attribute associates a named local type in the target language *repr-type* with a transfer type *named-type* that is transferred between client and server.</span></span>

``` syntax
typedef [represent_as(repr-type) [[ , type-attribute-list ]] ] named-type; 
void __RPC_USER named-type_from_local (
  repr-type __RPC_FAR * ,
  named-type __RPC_FAR * __RPC_FAR * );
void __RPC_USER named-type_to_local (
  named-type __RPC_FAR * ,
  repr-type __RPC_FAR * ); void __RPC_USER named-type _free_inst ( named-type __RPC_FAR * ); void __RPC_USER named-type _free_local ( repr-type __RPC_FAR * );
```

## <a name="parameters"></a><span data-ttu-id="4d884-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d884-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d884-107">*benannter Typ*</span><span class="sxs-lookup"><span data-stu-id="4d884-107">*named-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4d884-108">Gibt den benannten Übertragungs Datentyp an, der zwischen Client und Server übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="4d884-108">Specifies the named transfer data type that is transferred between client and server.</span></span>

</dd> <dt>

<span data-ttu-id="4d884-109">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4d884-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4d884-110">Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d884-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="4d884-111">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="4d884-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="4d884-112">*repr-Typ*</span><span class="sxs-lookup"><span data-stu-id="4d884-112">*repr-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4d884-113">Gibt den dargestellten lokalen Typ in der Zielsprache an, die den Client-und Server Anwendungen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4d884-113">Specifies the represented local type in the target language that is presented to the client and server applications.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d884-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d884-114">Remarks</span></span>

<span data-ttu-id="4d884-115">Wenn Sie **\[ \_ als \]** verwenden, müssen Sie Routinen bereitstellen, die zwischen dem lokalen und dem Übertragungs Typen konvertieren, und den freien Speicherplatz, der zum Speichern der konvertierten Daten verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4d884-115">When using **\[represent\_as\]**, you must supply routines that convert between the local and the transfer types and that free memory used to hold the converted data.</span></span> <span data-ttu-id="4d884-116">Das Attribut " **\[ \_ As \]** " weist die stubzeichen an, die vom Benutzer bereitgestellten Konvertierungs Routinen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4d884-116">The **\[represent\_as\]** attribute instructs the stubs to call the user-supplied conversion routines.</span></span>

<span data-ttu-id="4d884-117">Der übertragene Typ mit dem *Namen "-Type* " muss in einen mittleren Basistyp, einen vordefinierten Typ oder einen Typbezeichner aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="4d884-117">The transferred type *named-type* must resolve to a MIDL base type, predefined type, or to a type identifier.</span></span> <span data-ttu-id="4d884-118">Weitere Informationen finden Sie unter [Mittel l-Basis Typen](midl-base-types.md).</span><span class="sxs-lookup"><span data-stu-id="4d884-118">For more information, see [MIDL Base Types](midl-base-types.md).</span></span>

<span data-ttu-id="4d884-119">Sie müssen die folgenden Routinen angeben:</span><span class="sxs-lookup"><span data-stu-id="4d884-119">You must supply the following routines:</span></span>



| <span data-ttu-id="4d884-120">Routine Name</span><span class="sxs-lookup"><span data-stu-id="4d884-120">Routine name</span></span>                   | <span data-ttu-id="4d884-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d884-121">Description</span></span>                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d884-122">*benannter \_ Typ \* \* \* \_ from \_ local*\*</span><span class="sxs-lookup"><span data-stu-id="4d884-122">*named\_type\*\*\*\_from\_local*\*</span></span> | <span data-ttu-id="4d884-123">Konvertiert Daten aus dem lokalen Typ in den Netzwerktyp.</span><span class="sxs-lookup"><span data-stu-id="4d884-123">Converts data from the local type to the network type.</span></span> <span data-ttu-id="4d884-124">Die Routine ordnet Arbeitsspeicher für den Netzwerk Datentyp zu, einschließlich des Arbeitsspeichers für alle Daten, auf die von Zeigern im Netzwerk Datentyp verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4d884-124">The routine allocates memory for the network data type, including memory for any data referenced by pointers in the network data type.</span></span>              |
| <span data-ttu-id="4d884-125">*benannter \_ Typ \* \* \* \_ zu \_ lokal*\*</span><span class="sxs-lookup"><span data-stu-id="4d884-125">*named\_type\*\*\*\_to\_local*\*</span></span>   | <span data-ttu-id="4d884-126">Konvertiert Daten aus dem Netzwerktyp in den lokalen Typ.</span><span class="sxs-lookup"><span data-stu-id="4d884-126">Converts data from the network type to the local type.</span></span> <span data-ttu-id="4d884-127">Die Routine ist dafür verantwortlich, Arbeitsspeicher für Daten zuzuweisen, auf die von Zeigern im lokalen Typ verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4d884-127">The routine is responsible for allocating memory for data referenced by pointers in the local type.</span></span> <span data-ttu-id="4d884-128">RPC ordnet Speicher für den lokalen Typ selbst zu.</span><span class="sxs-lookup"><span data-stu-id="4d884-128">RPC allocates memory for the local type itself.</span></span> |
| <span data-ttu-id="4d884-129">*benannter \_ Typ \* \* \* \_ freie \_ lokale*\*</span><span class="sxs-lookup"><span data-stu-id="4d884-129">*named\_type\*\*\*\_free\_local*\*</span></span> | <span data-ttu-id="4d884-130">Gibt für Daten, auf die von Zeigern im lokalen Typ verwiesen wird, Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="4d884-130">Frees memory allocated for data referenced by pointers in the local type.</span></span> <span data-ttu-id="4d884-131">RPC gibt Arbeitsspeicher für den Typ selbst frei</span><span class="sxs-lookup"><span data-stu-id="4d884-131">RPC frees memory for the type itself</span></span>                                                                                             |
| <span data-ttu-id="4d884-132">*benannter \_ Typ \* \* \* \_ freie \_ inst*\*</span><span class="sxs-lookup"><span data-stu-id="4d884-132">*named\_type\*\*\*\_free\_inst*\*</span></span>  | <span data-ttu-id="4d884-133">Gibt Speicherplatz frei, der für die Daten, auf die von Zeigern im Netzwerktyp verwiesen wird, und für den Netzwerktyp</span><span class="sxs-lookup"><span data-stu-id="4d884-133">Frees memory allocated for the data referenced by pointers in the network type and for the network type itself.</span></span>                                                                                            |



 

<span data-ttu-id="4d884-134">Der Clientstub Ruft den *benannten Typ \* \* \* \_ aus \_ local*\* auf, um Speicherplatz für den übertragenen Typ zuzuweisen und die Daten vom lokalen Typ in den Netzwerktyp zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="4d884-134">The client stub calls *named-type\*\*\*\_from\_local*\* to allocate space for the transmitted type and to translate the data from the local type to the network type.</span></span> <span data-ttu-id="4d884-135">Der Serverstub ordnet Speicherplatz für den ursprünglichen Datentyp zu und ruft den *benannten Typ \* \* \* \_ auf \_ local*\* auf, um die Daten vom Netzwerktyp in den lokalen Typ zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="4d884-135">The server stub allocates space for the original data type and calls *named-type\*\*\*\_to\_local*\* to translate the data from the network type to the local type.</span></span>

<span data-ttu-id="4d884-136">Bei Rückgabe aus dem Anwendungscode ruft der Client-und der Server-Stub den \*Namen "-Type \* \* \* \_ Free \_ inst\*\*" auf, um die Speicherplatz Zuteilung für den Netzwerktyp freizugeben.</span><span class="sxs-lookup"><span data-stu-id="4d884-136">Upon return from the application code, the client and server stubs call *named-type\*\*\*\_free\_inst*\* to deallocate the storage for network type.</span></span> <span data-ttu-id="4d884-137">Der Clientstub Ruft den *benannten Typ \* \* \* \_ Free \_ local*\* auf, um die Speicher Belegungs Daten zuzuweisen, die von der Routine zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4d884-137">The client stub calls *named-type\*\*\*\_free\_local*\* to deallocate storage returned by the routine.</span></span>

<span data-ttu-id="4d884-138">Die folgenden Typen dürfen kein **\[ \_ als \]** -Attribut darstellen:</span><span class="sxs-lookup"><span data-stu-id="4d884-138">The following types cannot have a **\[represent\_as\]** attribute:</span></span>

-   <span data-ttu-id="4d884-139">Konforme, abweichende oder konforme Arrays</span><span class="sxs-lookup"><span data-stu-id="4d884-139">Conformant, varying, or conformant-varying arrays</span></span>
-   <span data-ttu-id="4d884-140">Strukturen, bei denen der letzte Member ein konformes Array ist (eine konforme Struktur)</span><span class="sxs-lookup"><span data-stu-id="4d884-140">Structures in which the last member is a conformant array (a conformant structure)</span></span>
-   <span data-ttu-id="4d884-141">Zeiger oder Typen, die einen Zeiger enthalten</span><span class="sxs-lookup"><span data-stu-id="4d884-141">Pointers or types that contain a pointer</span></span>
-   <span data-ttu-id="4d884-142">Pipes oder Typen, die Pipes enthalten</span><span class="sxs-lookup"><span data-stu-id="4d884-142">Pipes or types that contain pipes</span></span>
-   <span data-ttu-id="4d884-143">Typen, die als Basistyp für eine Pipe verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4d884-143">Types that are used as the base type for a pipe</span></span>
-   <span data-ttu-id="4d884-144">Vordefinierte Typen [**handle \_ t**](handle-t.md), [**void**](void.md)</span><span class="sxs-lookup"><span data-stu-id="4d884-144">Predefined types [**handle\_t**](handle-t.md), [**void**](void.md)</span></span>
-   <span data-ttu-id="4d884-145">Typen, die über das [**\[ handle \]**](handle.md) -Attribut verfügen</span><span class="sxs-lookup"><span data-stu-id="4d884-145">Types that have the [**\[handle\]**](handle.md) attribute</span></span>

## <a name="examples"></a><span data-ttu-id="4d884-146">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d884-146">Examples</span></span>

``` syntax
//these data types defined in .IDL or elsewhere
typedef struct  _lbox 
{ 
    long         data; 
    struct _lbox *next; 
} lbox; 
typedef [ref] lbox *PBOX_LOC; 
typedef long LONG4[4]; 
 
//in .ACF file :
interface iface
{
    typedef  [ represent_as(PBOX_LOC) ]  LONG4; 
}
```

## <a name="see-also"></a><span data-ttu-id="4d884-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4d884-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d884-148">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="4d884-148">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="4d884-149">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="4d884-149">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="4d884-150">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="4d884-150">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="4d884-151">**Handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="4d884-151">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="4d884-152">**typedef**</span><span class="sxs-lookup"><span data-stu-id="4d884-152">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="4d884-153">**void**</span><span class="sxs-lookup"><span data-stu-id="4d884-153">**void**</span></span>](void.md)
</dt> </dl>

 

 




