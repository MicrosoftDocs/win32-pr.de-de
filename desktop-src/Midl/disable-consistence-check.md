---
title: disable_consistency_check-Attribut
description: Weist RPC an, keine Korrelations Konsistenzprüfung zu erzwingen.
ms.assetid: 33ba331d-56e5-4965-a844-7780ea81623d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc55197b5eb680533745a09d4fca4f5827574a7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309564"
---
# <a name="disable_consistency_check-attribute"></a><span data-ttu-id="9e7da-103">\_Attribut für Konsistenz \_ Prüfung deaktivieren</span><span class="sxs-lookup"><span data-stu-id="9e7da-103">disable\_consistency\_check Attribute</span></span>

<span data-ttu-id="9e7da-104">Weist RPC an, keine Korrelations Konsistenzprüfung zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="9e7da-104">Directs RPC to not enforce correlation consistency checking.</span></span>

``` syntax
interface interface-name
{
  return-type function-name(
        [[attribute-list,] disable_consistency_check] param-type param-name
}
```

<span data-ttu-id="9e7da-105">Bei korrelierten Parametern erzwingt RPC, dass ein nicht-NULL-Puffer übermittelt wird, wenn die Korrelations Anzahl Variable nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="9e7da-105">For correlated parameters, RPC will enforce that a non-null buffer is passed when the correlation count variable is non-null.</span></span>

## <a name="example"></a><span data-ttu-id="9e7da-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9e7da-106">Example</span></span>

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, 
    size_is( Length )]LPWSTR MyString );
```

<span data-ttu-id="9e7da-107">Wenn *MyString* **null** ist, lehnt RPC den Aufruf ab, sofern die Länge nicht auf 0 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9e7da-107">If *MyString* is **NULL**, RPC will reject the call unless Length is set to 0.</span></span> <span data-ttu-id="9e7da-108">Beachten Sie, dass RPC eine *Länge* von 0 (null) zulässt, während *MyString* nicht NULL ist, und RPC behandelt *MyString* als Puffer Zuordnung mit einer Länge von 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9e7da-108">Note that RPC will allow *Length* to be 0 while *MyString* is non-NULL, and RPC will treat *MyString* as a 0-length buffer allocation.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e7da-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e7da-109">Remarks</span></span>

<span data-ttu-id="9e7da-110">Um diese Überprüfung zu deaktivieren, kann die IDL das \[ Attribut zum Deaktivieren der \_ Konsistenz \_ Prüfung \] für einen Parameter, eine typedef oder einen Zeigertyp enthalten.</span><span class="sxs-lookup"><span data-stu-id="9e7da-110">To disable this checking, the IDL can contain the \[disable\_consistency\_check\] attribute on a parameter, typedef, or pointer type.</span></span> <span data-ttu-id="9e7da-111">Dadurch wird RPC umgeleitet, um die Konsistenz zwischen dem Puffer Zeiger und der Korrelations Variablen für den Puffer, auf den der-Parameter oder-Zeiger zeigt, nicht zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="9e7da-111">This will direct RPC to not enforce the consistency between the buffer pointer and the correlation variable for the buffer pointed to by the parameter or pointer.</span></span>

<span data-ttu-id="9e7da-112">Um die Konsistenzprüfung für eine vollständige Mittel l-Kompilierung zu deaktivieren (und die Erzwingung der Überprüfung in allen Fällen zu deaktivieren), kann der Befehl für die Mittel l-Befehlszeile [/Backward \_ Kompatibilitäts maybenull \_ sizeis](-backward-compat.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e7da-112">To disable consistency checking for an entire MIDL compilation (and disable enforcement of the checking in all cases), the MIDL command line switch [/backward\_compat maybenull\_sizeis](-backward-compat.md) can be used.</span></span> <span data-ttu-id="9e7da-113">Hierfür ist es erforderlich, dass das Ziel der Mittell-Kompilierung mindestens "target nt60" ist.</span><span class="sxs-lookup"><span data-stu-id="9e7da-113">This requires that the target of the MIDL compilation be at least â€“target NT60.</span></span>

 

 




