---
title: Verfügbar machen zusätzlicher Informationen, die nicht von der IAccessible-Schnittstelle
description: Abhängig von ihren Produkten müssen Server Entwickler möglicherweise zusätzlich zum Microsoft Active Accessibility-Support Informationen oder Funktionen verfügbar machen.
ms.assetid: c45009ca-6be3-4645-9097-36671a41dfce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3834c60de8f18fd5ec0719919a1cd79e22f451e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316028"
---
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a><span data-ttu-id="ab0dd-103">Verfügbar machen zusätzlicher Informationen, die nicht von der IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ab0dd-103">Exposing Additional Information Not Covered by IAccessible Interface</span></span>

<span data-ttu-id="ab0dd-104">Abhängig von ihren Produkten müssen Server Entwickler möglicherweise zusätzlich zum Microsoft Active Accessibility-Support Informationen oder Funktionen verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="ab0dd-104">Depending on their products, server developers might need to expose information or functionality in addition to Microsoft Active Accessibility support.</span></span> <span data-ttu-id="ab0dd-105">Wenn dies der Fall ist, können Sie mit hilfstechnologieanbietern (Clients) zusammenarbeiten, um sicherzustellen, dass Sie Unterstützung für die Features hinzufügen</span><span class="sxs-lookup"><span data-stu-id="ab0dd-105">If this is the case, work with assistive technology vendors (clients) to ensure that they add support for the features.</span></span>

<span data-ttu-id="ab0dd-106">Versuchen Sie nicht, die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="ab0dd-106">Do not attempt to extend the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="ab0dd-107">Schnittstellen können nicht geändert werden, sobald Sie veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="ab0dd-107">Interfaces cannot be changed once they are published.</span></span> <span data-ttu-id="ab0dd-108">Um zusätzliche Informationen verfügbar zu machen, verwenden Sie eine benutzerdefinierte Schnittstelle, und machen Sie Sie mithilfe einer der folgenden Methoden verfügbar:</span><span class="sxs-lookup"><span data-stu-id="ab0dd-108">To expose additional information, use a custom interface and expose it by using one of the following techniques:</span></span>

-   [<span data-ttu-id="ab0dd-109">Verwenden von objID \_ nativeom, um eine systemeigene Objektmodell Schnittstelle für ein Fenster verfügbar zu machen</span><span class="sxs-lookup"><span data-stu-id="ab0dd-109">Using OBJID\_NATIVEOM to expose a native object model interface for a window</span></span>](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [<span data-ttu-id="ab0dd-110">Verwenden von QueryService, um eine systemeigene Objektmodell Schnittstelle für ein IAccessible-Objekt verfügbar zu machen</span><span class="sxs-lookup"><span data-stu-id="ab0dd-110">Using QueryService to expose a native object model interface for an IAccessible object</span></span>](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

<span data-ttu-id="ab0dd-111">Beachten Sie, dass das Ziel der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle darin besteht, eine klar definierte Schnittstelle zu verwenden, die von Servern und Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab0dd-111">Note that the goal of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is to have a well-defined interface that is used by servers and clients.</span></span> <span data-ttu-id="ab0dd-112">Bevor Sie benutzerdefinierte Schnittstellen verfügbar machen, stellen Sie sicher, dass Sie so viele Informationen wie möglich über **IAccessible verfügbar** machen</span><span class="sxs-lookup"><span data-stu-id="ab0dd-112">Before exposing custom interfaces, be sure to expose as much information as possible through **IAccessible**.</span></span>

<span data-ttu-id="ab0dd-113">Sie können [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) nicht verwenden, um benutzerdefinierte Schnittstellen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ab0dd-113">You cannot use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to expose custom interfaces.</span></span> <span data-ttu-id="ab0dd-114">Verwenden Sie **IServiceProvider:: QueryService** , wie in den folgenden Prozeduren beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ab0dd-114">Use **IServiceProvider::QueryService** as outlined in the following procedures.</span></span>

 

 