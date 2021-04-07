---
title: Bereiche Verarbeitung und Attribut Bearbeitung
description: Die Verarbeitung von Bereichen, die auch als Attribut Manipulation bezeichnet wird, bezieht sich auf das Transformieren des Namens des Benutzers, der Zugriff anfordert.
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd630fd683342c45ab35161bf2c740ac7e8a6fa2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728568"
---
# <a name="realms-processing-and-attribute-manipulation"></a>Bereiche Verarbeitung und Attribut Bearbeitung

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

Die Verarbeitung von Bereichen, die auch als Attribut Manipulation bezeichnet wird, bezieht sich auf das Transformieren des Namens des Benutzers, der Zugriff anfordert. Die aufrufende-ID und die ID der aufgerufenen Station können ebenfalls manipuliert werden. Die Bereichs Verarbeitungs Regeln sind Teil der Auflistung der Proxy Profil Attribute.

Für jede Bearbeitung müssen Sie zwei [Manipulations Regel](/windows/desktop/Nps/sdo-manipulation-rule) Attribute erstellen. Jedes dieser Attribute ist ein Zeichen folgen Wert. Die erste Regel enthält einen regulären Ausdruck, der das Muster darstellt, das abgeglichen werden soll. Die zweite Regel enthält einen regulären Ausdruck, der den Ersetzungstext darstellt. Außerdem müssen Sie ein [Manipulations Ziel](/windows/desktop/Nps/sdo-manipulation-target) Attribut erstellen. Dieses Attribut ist eine Enumeration, die angibt, welcher Teil der Benutzerinformationen bearbeitet werden soll.

Die Reihenfolge, in der die Attribute erstellt werden, ist wichtig. NPS verarbeitet die Attribute in der Reihenfolge, in der Sie erstellt wurden.

Die folgende Tabelle zeigt ein Beispiel für eine Reihe von Manipulations Attributen.



| Name                 | type         | Zeichenfolgenwert     |
|----------------------|--------------|------------------|
| msmanipulationrule   | **VT \_ BSTR** | "@company.com"   |
| msmanipulationrule   | **VT \_ BSTR** | "@microsoft.com" |
| msmanipulationrule   | **VT \_ BSTR** | "^.+@"           |
| msmanipulationrule   | **VT \_ BSTR** | "Guest@"         |
| msmanipulationtarget | **VT \_ I4**   | "1"              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Objektmodell Hierarchie](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[Unterstützte SDO-Attribute](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[Erstellen einer Verbindungs Anforderungs Richtlinie](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[**Isdocollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[**Isdodiktattionaryold**](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[**Iasproperties**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 