---
title: Out-Only eindeutige oder vollständige Zeiger Parameter nicht akzeptiert.
description: Eindeutige oder vollständige Zeiger, bei denen es sich nicht um \ out handelt, werden vom Mittelwert Compiler nicht akzeptiert. Diese Spezifikationen bewirken, dass der Mittell-Compiler eine Fehlermeldung generiert.
ms.assetid: 0477980e-d76e-452f-9ab1-71a8ed8642d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b21baa370c1b68fb3c708a8fdb21115686646f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516976"
---
# <a name="out-only-unique-or-full-pointer-parameters-not-accepted"></a><span data-ttu-id="b0e3e-104">Out-Only eindeutige oder vollständige Zeiger Parameter nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-104">Out-Only Unique or Full Pointer Parameters Not Accepted</span></span>

<span data-ttu-id="b0e3e-105">Eindeutige oder vollständige Zeiger, die nicht als veraltet gelten, \[ [](/windows/desktop/Midl/out-idl) \] werden vom Mittelwert Compiler nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-105">Unique or full pointers that are \[ [out](/windows/desktop/Midl/out-idl)\]-only are not accepted by the MIDL compiler.</span></span> <span data-ttu-id="b0e3e-106">Diese Spezifikationen bewirken, dass der Mittell-Compiler eine Fehlermeldung generiert.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-106">Such specifications cause the MIDL compiler to generate an error message.</span></span>

<span data-ttu-id="b0e3e-107">Der automatisch generierte Serverstub muss Speicher für den Zeiger Referenten zuweisen, damit die Serveranwendung Daten in diesem Speicherbereich speichern kann.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-107">The automatically generated server stub has to allocate memory for the pointer referent so that the server application can store data in that memory area.</span></span> <span data-ttu-id="b0e3e-108">Gemäß der Definition eines reinen **\[ out \]**-Parameters werden keine Informationen über den-Parameter vom Client an den Server übertragen.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-108">According to the definition of an **\[out\]**-only parameter, no information about the parameter is transmitted from client to server.</span></span> <span data-ttu-id="b0e3e-109">Im Fall eines eindeutigen Zeigers, der den Wert NULL annehmen kann, verfügt der Serverstub nicht über genügend Informationen zum korrekten Duplizieren des eindeutigen Zeigers im Adressraum des Servers, und der Stub hat keine Informationen darüber, ob der Zeiger auf eine gültige Adresse zeigen soll oder ob er auf NULL festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-109">In the case of a unique pointer, which can take the value null, the server stub does not have enough information to correctly duplicate the unique pointer in the server's address space, nor does the stub have any information about whether the pointer should point to a valid address or whether it should be set to null.</span></span> <span data-ttu-id="b0e3e-110">Daher ist diese Kombination nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-110">Therefore, this combination is not allowed.</span></span>

<span data-ttu-id="b0e3e-111">Anstatt \[ **out**, [Unique](/windows/desktop/Midl/unique) \] oder \[ **out**, [ptr](/windows/desktop/Midl/ptr) \] -Zeiger, use \[ **in**, **out**, **Unique** \] oder \[ **in**, **out**, **ptr** - \] Zeiger, oder verwenden Sie eine andere Dereferenzierungsebene, z. b. einen Verweis Zeiger, der auf den gültigen eindeutigen oder vollständigen Zeiger zeigt.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-111">Rather than \[**out**, [unique](/windows/desktop/Midl/unique)\] or \[**out**, [ptr](/windows/desktop/Midl/ptr)\] pointers, use \[**in**, **out**, **unique**\] or \[**in**, **out**, **ptr**\] pointers, or use another level of indirection such as a reference pointer that points to the valid unique or full pointer.</span></span>

 

 