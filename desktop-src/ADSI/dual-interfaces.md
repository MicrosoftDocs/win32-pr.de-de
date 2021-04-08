---
title: Duale Schnittstellen (ADSI)
description: Verwenden Sie COM-Schnittstellen, um auf die Eigenschaften und Methoden von ADSI-Objekten eines Anbieters zuzugreifen.
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34c858275098dd82362d229bc9e1cc35b544c55
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730185"
---
# <a name="dual-interfaces-adsi"></a>Duale Schnittstellen (ADSI)

Verwenden Sie COM-Schnittstellen, um auf die Eigenschaften und Methoden von ADSI-Objekten eines Anbieters zuzugreifen. Eine schreibgeschützte Eigenschaft wird einem Schnittstellen Eintrag im Formular **get \_ <PropertyName>** zugeordnet. Eine Eigenschaft mit Lese-/Schreibzugriff wird zwei Schnittstellen Einträgen im Formular **get \_ <PropertyName>** und **Put \_ <PropertyName>** zugeordnet.

Alle Methoden einer COM-Schnittstelle müssen folgende Aktionen ausführen:

-   Gibt einen HRESULT-Wert zurück, der den Erfolg oder Misserfolg angibt. Der **HRESULT** -Typ wird in der com-Spezifikation erläutert.
-   Gibt bei Aufrufen von **QueryInterface** **E \_ nointerface** für nicht implementierte Schnittstellen zurück.
-   Gibt **E \_ notimpl** für nicht implementierte Methoden für Schnittstellen zurück, die anderweitig implementiert werden.
-   Die Rückgabe der E ADS-Eigenschaft wird für nicht unterstützte Schnittstelleneigenschaften **\_ \_ \_ nicht \_ unterstützt** .

Um die Kompatibilität mit Automatisierungs Controllern beizubehalten, sollten alle Parameter und Rückgabe Typen in der Teilmenge liegen, die durch den Datentyp "Automation Variant" definiert wird. Weitere Informationen finden Sie unter **Variant** und **VARIANTARG** im Platform Software Development Kit (SDK).

Ein Anbieter Active Directory-Objekt kann Schnittstellen verfügbar machen, die andere Datentypen als die in der **Variant** -Teilmenge verwenden. Automatisierungs Controller wie Visual Basic können diese Schnittstellen jedoch nicht aufzurufen. Die meisten ADSI-Anbieter Schnittstellen werden von [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) abgeleitet und können als **IDispatch** -Schnittstellen Zeiger verwendet werden. Die ADSI-Schnittstellen [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)und [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension) werden jedoch nicht von **IDispatch** abgeleitet.

 

 