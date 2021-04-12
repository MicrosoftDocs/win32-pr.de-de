---
title: midl_user_allocate-Attribut
description: Die Funktion "Mittelwert \_ Benutzer \_ zuweisen" ist eine Funktion, die Client-und Server Anwendungen bereitstellen, um Speicher zuzuweisen.
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- midl_user_allocate Attribut-Mittel l
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4be10c5e1c7073afb3abf359c3ec2fb79a4335b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315062"
---
# <a name="midl_user_allocate-attribute"></a><span data-ttu-id="c7167-104">Attribut "Mittel l- \_ Benutzer \_ zuweisen"</span><span class="sxs-lookup"><span data-stu-id="c7167-104">midl\_user\_allocate attribute</span></span>

<span data-ttu-id="c7167-105">Die Funktion " **Mittelwert \_ Benutzer \_ zuweisen** " ist eine Funktion, die Client-und Server Anwendungen bereitstellen, um Speicher zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="c7167-105">The **midl\_user\_allocate** function is a function that client and server applications provide to allocate memory.</span></span>

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a><span data-ttu-id="c7167-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7167-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7167-107">*cbytes*</span><span class="sxs-lookup"><span data-stu-id="c7167-107">*cBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="c7167-108">Gibt die Anzahl der zuzuordnenden Bytes an.</span><span class="sxs-lookup"><span data-stu-id="c7167-108">Specifies the count of bytes to allocate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7167-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7167-109">Remarks</span></span>

<span data-ttu-id="c7167-110">Sowohl Client Anwendungen als auch Server Anwendungen müssen die Funktion " **mittlere \_ \_ Benutzer** Zuordnungen" implementieren, es sei denn, Sie kompilieren ihn im OSF-Kompatibilitätsmodus ([**/OSF**](-osf.md)).</span><span class="sxs-lookup"><span data-stu-id="c7167-110">Both client applications and server applications must implement the **midl\_user\_allocate** function, unless you are compiling in OSF-compatibility ([**/osf**](-osf.md)) mode.</span></span> <span data-ttu-id="c7167-111">Anwendungen und generierte stubzeichen wenden beim Umgang mit Objekten, auf die von Zeigern verwiesen wird, eine **mittlere \_ Benutzer \_ Zuteilung** an</span><span class="sxs-lookup"><span data-stu-id="c7167-111">Applications and generated stubs call **midl\_user\_allocate** when dealing with objects referenced by pointers:</span></span>

-   <span data-ttu-id="c7167-112">Die Serveranwendung sollte bei der Erstellung eines neuen Knotens für die Application-Klasse den Befehl " **Mittel l- \_ Benutzer \_ zuweisen** " anrufen.</span><span class="sxs-lookup"><span data-stu-id="c7167-112">The server application should call **midl\_user\_allocate** to allocate memory for the applicationâ€”for example, when creating a new node.</span></span>
-   <span data-ttu-id="c7167-113">Der Serverstub Ruft beim Marshalling von referenzierten Daten in den Adressraum des Servers die Benutzer Zuordnungen für **mittellose \_ Benutzer \_** auf.</span><span class="sxs-lookup"><span data-stu-id="c7167-113">The server stub calls **midl\_user\_allocate** when unmarshaling pointed-at data into the server address space.</span></span>
-   <span data-ttu-id="c7167-114">Der Clientstub Ruft bei der Aufhebung des Marshalling von Daten von dem Server, auf den von einem [**out**](out-idl.md) -Zeiger verwiesen wird, die Benutzer Zuordnungen für **mittlere \_ Benutzer \_** auf</span><span class="sxs-lookup"><span data-stu-id="c7167-114">The client stub calls **midl\_user\_allocate** when unmarshaling data from the server that is referenced by an [**out**](out-idl.md) pointer.</span></span> <span data-ttu-id="c7167-115">Beachten Sie, dass **\[** [](in.md) **\]** der Client-Stub bei in-, **\[ \] out**-und **\[** [**Unique**](unique.md) **\]** -Zeigern nur dann die **\_ Benutzer \_** Zuordnungen aufruft, wenn der **\[ eindeutige \]** Zeiger Wert bei Eingabe **null** war und während des Aufrufs zu einem Wert ungleich **null** wechselt.</span><span class="sxs-lookup"><span data-stu-id="c7167-115">Note that for **\[**[**in**](in.md)**\]**, **\[out\]**, and **\[**[**unique**](unique.md)**\]** pointers, the client stub calls **midl\_user\_allocate** only if the **\[unique\]** pointer value was **NULL** on input and changes to a non-**NULL** value during the call.</span></span> <span data-ttu-id="c7167-116">Wenn der **\[ eindeutige \]** Zeiger bei Eingabe ungleich **null** war, schreibt der Clientstub die zugeordneten Daten in den vorhandenen Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c7167-116">If the **\[unique\]** pointer was non-**NULL** on input, the client stub writes the associated data into existing memory.</span></span>

<span data-ttu-id="c7167-117">Wenn die Zuordnungen von **\_ Benutzer \_** Zuordnungen keinen Arbeitsspeicher zuordnen können, muss ein **null** -Zeiger zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c7167-117">If **midl\_user\_allocate** fails to allocate memory, it must return a **NULL** pointer.</span></span>

<span data-ttu-id="c7167-118">Es wird empfohlen, dass die Benutzer Zuordnungen in der Mitte einen Zeiger zurückgeben, der auf 8 Bytes ausgerichtet ist. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="c7167-118">It is recommended that **midl\_user\_allocate** return a pointer that is 8 bytes aligned.</span></span>

## <a name="examples"></a><span data-ttu-id="c7167-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7167-119">Examples</span></span>


```C++
#include <windows.h>

void __RPC_FAR * __RPC_API midl_user_allocate(size_t cBytes) 
{ 
    return(malloc(cBytes)); 
}
```



## <a name="see-also"></a><span data-ttu-id="c7167-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c7167-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7167-121">**allocate**</span><span class="sxs-lookup"><span data-stu-id="c7167-121">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="c7167-122">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="c7167-122">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="c7167-123">Arrays und Zeiger</span><span class="sxs-lookup"><span data-stu-id="c7167-123">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="c7167-124">Array-und Sized-Pointer Attribute</span><span class="sxs-lookup"><span data-stu-id="c7167-124">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="c7167-125">**in**</span><span class="sxs-lookup"><span data-stu-id="c7167-125">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="c7167-126">**mittlerer l- \_ Benutzer \_ kostenlos**</span><span class="sxs-lookup"><span data-stu-id="c7167-126">**midl\_user\_free**</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="c7167-127">**/osf**</span><span class="sxs-lookup"><span data-stu-id="c7167-127">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="c7167-128">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="c7167-128">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="c7167-129">**ptr**</span><span class="sxs-lookup"><span data-stu-id="c7167-129">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="c7167-130">**ref**</span><span class="sxs-lookup"><span data-stu-id="c7167-130">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="c7167-131">**gem**</span><span class="sxs-lookup"><span data-stu-id="c7167-131">**unique**</span></span>](unique.md)
</dt> </dl>

 

 