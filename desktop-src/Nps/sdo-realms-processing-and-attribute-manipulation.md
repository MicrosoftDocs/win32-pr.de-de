---
title: Bereichsverarbeitung und Attributbearbeitung
description: Bereichsverarbeitung, die auch als Attributbearbeitung bezeichnet wird, bezieht sich auf das Transformieren des Namens des Benutzers, der Zugriff an fordert.
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8054ad8234ca4772a52619d83bc85a9d357f2cf8da2f1c969eed918c75a8305a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618946"
---
# <a name="realms-processing-and-attribute-manipulation"></a>Bereichsverarbeitung und Attributbearbeitung

> [!Note]  
> Internet Authentication Service (IAS) wurde ab Windows Server 2008 in Network Policy Server (NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Diensts zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

Bereichsverarbeitung, die auch als Attributbearbeitung bezeichnet wird, bezieht sich auf das Transformieren des Namens des Benutzers, der Zugriff an fordert. Die ID der aufrufenden Station und die ID der aufgerufenen Station können ebenfalls bearbeitet werden. Die Bereichsverarbeitungsregeln sind Teil der Auflistung der Proxyprofilattribute.

Für jede Bearbeitung müssen Sie zwei [Manipulationsregelattribute](/windows/desktop/Nps/sdo-manipulation-rule) erstellen. Jedes dieser Attribute ist ein Zeichenfolgenwert. Die erste Regel enthält einen regulären Ausdruck, der das übereinstimmende Muster darstellt. Die zweite Regel enthält einen regulären Ausdruck, der den Ersetzungstext darstellt. Sie müssen auch ein [Manipulation-Target-Attribut](/windows/desktop/Nps/sdo-manipulation-target) erstellen. Dieses Attribut ist eine Enumeration, die angibt, welcher Teil der Benutzerinformationen bearbeitet werden soll.

Die Reihenfolge, in der die Attribute erstellt werden, ist wichtig. NPS verarbeitet die Attribute in der Reihenfolge, in der sie erstellt wurden.

Die folgende Tabelle zeigt ein Beispiel für einen Satz von Manipulationsattributen.



| Name                 | type         | Zeichenfolgenwert     |
|----------------------|--------------|------------------|
| msManipulationRule   | **VT \_ BSTR** | "@company.com"   |
| msManipulationRule   | **VT \_ BSTR** | "@microsoft.com" |
| msManipulationRule   | **VT \_ BSTR** | "^.+@"           |
| msManipulationRule   | **VT \_ BSTR** | "guest@"         |
| msManipulationTarget | **VT \_ I4**   | "1"              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Objektmodellhierarchie](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[Von SDO unterstützte Attribute](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[Erstellen einer Verbindungsanforderungsrichtlinie](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[**ISdoDictionaryOld**](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 