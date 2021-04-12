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
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a>Verfügbar machen zusätzlicher Informationen, die nicht von der IAccessible-Schnittstelle

Abhängig von ihren Produkten müssen Server Entwickler möglicherweise zusätzlich zum Microsoft Active Accessibility-Support Informationen oder Funktionen verfügbar machen. Wenn dies der Fall ist, können Sie mit hilfstechnologieanbietern (Clients) zusammenarbeiten, um sicherzustellen, dass Sie Unterstützung für die Features hinzufügen

Versuchen Sie nicht, die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle zu erweitern. Schnittstellen können nicht geändert werden, sobald Sie veröffentlicht wurden. Um zusätzliche Informationen verfügbar zu machen, verwenden Sie eine benutzerdefinierte Schnittstelle, und machen Sie Sie mithilfe einer der folgenden Methoden verfügbar:

-   [Verwenden von objID \_ nativeom, um eine systemeigene Objektmodell Schnittstelle für ein Fenster verfügbar zu machen](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [Verwenden von QueryService, um eine systemeigene Objektmodell Schnittstelle für ein IAccessible-Objekt verfügbar zu machen](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

Beachten Sie, dass das Ziel der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle darin besteht, eine klar definierte Schnittstelle zu verwenden, die von Servern und Clients verwendet wird. Bevor Sie benutzerdefinierte Schnittstellen verfügbar machen, stellen Sie sicher, dass Sie so viele Informationen wie möglich über **IAccessible verfügbar** machen

Sie können [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) nicht verwenden, um benutzerdefinierte Schnittstellen bereitzustellen. Verwenden Sie **IServiceProvider:: QueryService** , wie in den folgenden Prozeduren beschrieben.

 

 