---
title: Duale Schnittstellen (ADSI)
description: Verwenden Sie COM-Schnittstellen, um auf die Eigenschaften und Methoden für ADSI-Anbieterobjekte zu zugreifen.
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d1cf89ef07e573be8f59805034ff8c567e75fd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884055"
---
# <a name="dual-interfaces-adsi"></a>Duale Schnittstellen (ADSI)

Verwenden Sie COM-Schnittstellen, um auf die Eigenschaften und Methoden für ADSI-Anbieterobjekte zu zugreifen. Eine schreibgeschützte Eigenschaft wird einem Schnittstelleneintrag im Formular **get \_ &lt; PropertyName zu. &gt;** Eine Lese-/Schreibeigenschaft wird zwei Schnittstelleneinträgen im Formular **get \_ &lt; PropertyName &gt;** und **put \_ &lt; PropertyNamezur Verfügung. &gt;**

Alle Methoden auf einer COM-Schnittstelle müssen:

-   Gibt einen HRESULT-Wert zurück, der auf Erfolg oder Fehler hinweist. Der **HRESULT-Typ** wird in der COM-Spezifikation erläutert.
-   Geben Sie bei **Aufrufen von QueryInterface** **E \_ NOINTERFACE** für nicht implementierte Schnittstellen zurück.
-   Gibt **E \_ NOTIMPL** für nicht implementierte Methoden auf Schnittstellen zurück, die andernfalls implementiert werden.
-   Gibt **E ADS PROPERTY NOT SUPPORTED \_ \_ \_ \_ für** Schnittstelleneigenschaften zurück, die nicht unterstützt werden.

Um die Kompatibilität mit Automation-Controllern zu gewährleisten, sollten alle Parameter und Rückgabetypen innerhalb der Teilmenge sein, die vom Automation VARIANT-Datentyp definiert wird. Weitere Informationen finden Sie unter **VARIANT** und **VARIANTARG** im Platform Software Development Kit (SDK).

Ein Active Directory-Anbieterobjekt kann Schnittstellen verfügbar machen, die andere Datentypen als die in der **VARIANT-Teilmenge** verwenden. Automatisierungscontroller wie Visual Basic können diese Schnittstellen jedoch nicht aufrufen. Die meisten ADSI-Anbieterschnittstellen werden von [**IDispatch abgeleitet**](/windows/win32/api/oaidl/nn-oaidl-idispatch) und können als **IDispatch-Schnittstellenzeler** verwendet werden. Die [**ADSI-Schnittstellen IDirectoryObject,**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)und [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) werden jedoch nicht von **IDispatch abgeleitet.**

 

 
