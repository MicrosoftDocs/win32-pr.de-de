---
title: Mittel l-Bindungs Handles
description: Bindungs Handles sind Datenobjekte, die die Bindung zwischen Client und Server darstellen.
ms.assetid: 178f4838-3deb-43d4-804f-ad6404b377bd
keywords:
- Datentypen-Mittel l, Bindungs Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59faea2137cb037cab1e5969e53fff2c146ad31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038822"
---
# <a name="midl-binding-handles"></a><span data-ttu-id="1ecd0-104">Mittel l-Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="1ecd0-104">MIDL Binding Handles</span></span>

<span data-ttu-id="1ecd0-105">Bindungs Handles sind Datenobjekte, die die Bindung zwischen Client und Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="1ecd0-105">Binding handles are data objects that represent the binding between the client and the server.</span></span>

<span data-ttu-id="1ecd0-106">"Mittel l" unterstützt das Basistyp [**handle \_ t**](handle-t.md).</span><span class="sxs-lookup"><span data-stu-id="1ecd0-106">MIDL supports the base type [**handle\_t**](handle-t.md).</span></span> <span data-ttu-id="1ecd0-107">Handles dieses Typs werden als "primitive Handles" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1ecd0-107">Handles of this type are known as "primitive handles."</span></span>

<span data-ttu-id="1ecd0-108">Mit dem **\[ handle \]** -Attribut können Sie eigene handle-Typen definieren.</span><span class="sxs-lookup"><span data-stu-id="1ecd0-108">You can define your own handle types using the **\[handle\]** attribute.</span></span> <span data-ttu-id="1ecd0-109">Auf diese Weise definierte Handles werden als "benutzerdefinierte" oder "angepasste" oder "generische" Handles bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1ecd0-109">Handles defined in this way are known as "user-defined" or "customized" or "generic" handles.</span></span>

<span data-ttu-id="1ecd0-110">Sie können auch ein Handle definieren, das Zustandsinformationen mithilfe des **\[** [**Kontext \_ handle**](context-handle.md) - **\]** Attributs verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1ecd0-110">You can also define a handle that maintains state information using the **\[**[**context\_handle**](context-handle.md)**\]** attribute.</span></span> <span data-ttu-id="1ecd0-111">Auf diese Weise definierte Handles werden als "Kontext"-Handles bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1ecd0-111">Handles defined in this way are known as "context" handles.</span></span>

<span data-ttu-id="1ecd0-112">Wenn keine Zustandsinformationen erforderlich sind und Sie nicht auswählen, die RPC-Laufzeitbibliotheken zum Verwalten des Handles aufzurufen, können Sie anfordern, dass die Laufzeitbibliotheken eine automatische Bindung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1ecd0-112">If no state information is needed and you do not choose to call the RPC run-time libraries to manage the handle, you can request that the run-time libraries provide automatic binding.</span></span> <span data-ttu-id="1ecd0-113">Dies erfolgt mithilfe des automatischen ACF-Schlüssel Worts **\[** [**\_**](auto-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="1ecd0-113">This is done by using the ACF keyword **\[**[**auto\_handle**](auto-handle.md)**\]**.</span></span>

<span data-ttu-id="1ecd0-114">Sie können eine globale Variable als Bindungs Handle angeben, indem Sie das implizite ACF-Schlüsselwort **\[** [**\_ handle**](implicit-handle.md)verwenden **\]** .</span><span class="sxs-lookup"><span data-stu-id="1ecd0-114">You can specify a global variable as the binding handle by using the ACF keyword **\[**[**implicit\_handle**](implicit-handle.md)**\]**.</span></span> <span data-ttu-id="1ecd0-115">Mit dem **\[ expliziten \_ handle \]** -Schlüsselwort wird festgelegt, dass jede Remote Funktion über ein explizit angegebenes Handle verfügt.</span><span class="sxs-lookup"><span data-stu-id="1ecd0-115">The **\[explicit\_handle\]** keyword is used to state that each remote function has an explicitly specified handle.</span></span>

<span data-ttu-id="1ecd0-116">Weitere Informationen finden Sie unter [Bindung und Handles](/windows/desktop/Rpc/binding-and-handles).</span><span class="sxs-lookup"><span data-stu-id="1ecd0-116">For more information, see [Binding and Handles](/windows/desktop/Rpc/binding-and-handles).</span></span>

 

 