---
title: Benutzeroberflächen Erweiterung für neue Objektklassen
description: Active Directory Domain Services und die zugehörige Verwaltungs-MMC-Snap-in-Benutzeroberfläche können an die Anforderungen von Administratoren und Benutzern angepasst werden.
ms.assetid: 38e3b800-20ad-4da8-ad40-4e90838acfb5
ms.tgt_platform: multiple
keywords:
- Benutzeroberflächen Erweiterung für neue Objektklassen AD
- Objekt-AD, Benutzeroberflächen Erweiterung für neue Objektklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154b64a23eff72bf5751085a8e50691cd222abd6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947373"
---
# <a name="user-interface-extension-for-new-object-classes"></a>Benutzeroberflächen Erweiterung für neue Objektklassen

Active Directory Domain Services und die zugehörige Verwaltungs-MMC-Snap-in-Benutzeroberfläche können an die Anforderungen von Administratoren und Benutzern angepasst werden. Active Directory Domain Services das Ändern des Schemas durch Erstellen neuer Klassen und Attribute oder Ändern vorhandener Klassen ermöglichen. Anzeige Spezifizierungen für die Klassen können so geändert werden, dass Sie die neuen Benutzeroberflächen Elemente widerspiegeln, die für Schema Änderungen erforderlich sind.

In der folgenden Tabelle sind Attribute aufgeführt, mit denen Sie ändern können, wie das administrative Snap-in Objekte einer bestimmten Klasse anzeigt.



| Attribut                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **defaultHidingValue**     | Das **defaultHidingValue** -Attribut ist ein Attribut eines **classSchema** -Objekts. Dieses Attribut enthält einen booleschen Wert, der bei true bewirkt, dass Instanzen der Objektklasse in den administrativen Snap-Ins und in der Windows-Shell ausgeblendet werden. Dies bedeutet auch, dass ein Menü Element für die neue Objektklasse nicht im **neuen** Kontextmenü der administrativen Snap-Ins angezeigt wird, auch wenn die entsprechenden Eigenschaften des Erstellungs-Assistenten für das **Display specifier** -Objekt der neuen Objektklasse festgelegt sind. Wenn dieses Attribut false ist, werden Instanzen der Klasse in den administrativen Snap-Ins und in der Shell angezeigt. Dies bewirkt auch, dass ein Menü Element eine neue Objektinstanz erstellt, die dem **neuen** Menü der administrativen Snap-Ins hinzugefügt wird.<br/> Wenn für dieses Attribut kein Wert festgelegt ist, ist der Standardwert true. Dies bedeutet, dass Instanzen des-Objekts standardmäßig ausgeblendet werden.<br/>                                                                |
| **showInAdvancedViewOnly** | Das **showInAdvancedViewOnly** -Attribut enthält einen booleschen Wert, der bei true bewirkt, dass Instanzen der Objektklasse im Snap-in "Benutzer und Computer" nur in der erweiterten Ansicht angezeigt werden und nicht in der Windows-Shell angezeigt werden. Wenn diese Eigenschaft false ist, werden Instanzen der Klasse in der normalen Ansicht im Snap-in "Benutzer und Computer" und in der Windows-Shell angezeigt.<br/> Wenn für dieses Attribut kein Wert festgelegt ist, ist der Standardwert true.<br/> Dieses Attribut kann für ein einzelnes Objekt festgelegt werden, um den für die Objektklasse festgelegten Wert zu überschreiben. Beispielsweise ist für die **Container** -Klasse dieses Attribut auf "true" festgelegt, aber für den **Benutzer** Container ist dieser Wert auf "false" festgelegt. Aus diesem Grund wird der **Benutzer** Container in der Shell und in normaler Ansicht im Snap-in "Benutzer und Computer" angezeigt, aber andere Container, für die " **showInAdvancedViewOnly** " nicht auf "false" festgelegt ist, werden nur in der erweiterten Ansicht im Snap-in "Benutzer und Computer" angezeigt.<br/> |



 

## <a name="creating-display-specifiers-for-new-classes"></a>Erstellen von Anzeige spezifiken für neue Klassen

Um die Benutzeroberfläche für eine neue Klasse anzupassen, erstellen Sie ein anzeigespezifiziererobjekt für die neue Klasse für jedes unterstützte Gebiets Schema, und legen Sie dann die gewünschten Attribute für den Anzeigespezifizierer fest.

## <a name="inheriting-display-specifiers-for-derived-classes"></a>Erben von Anzeige spezifiken für abgeleitete Klassen

Eine neue Klasse, die von einer vorhandenen Klasse erbt, erbt nicht den Anzeige Spezifizierer der übergeordneten Klasse. Wenn es sich bei der neuen Klasse um das Verwenden einiger oder aller der Eigenschaften der übergeordneten Klassen Anzeige Spezifizierer handelt, erstellen Sie einen neuen Anzeigespezifizierer für die neue Klasse, und kopieren Sie die Eigenschaften des übergeordneten Klassen Anzeige Bezeichnern in den neuen objektanzeigespezifizierer. Dies muss für alle Gebiets Schemas erfolgen, für die die Anzeige spezifizierereigenschaften der übergeordneten Klasse gelten.

Bestimmte Teile der UI-Funktionsgruppe, z. b. die Menü Elemente und der Erstellungs-Assistent für die User-Klasse, werden intern implementiert und sind nicht für die Verwendung durch ein abgeleitetes Objekt verfügbar. In diesen Fällen ist es besser, eine vorhandene Klasse zu erweitern, als eine abgeleitete Klasse zu verwenden.

## <a name="modifying-existing-classes"></a>Ändern vorhandener Klassen

Neue Attribute können einer vorhandenen Klasse hinzugefügt werden. Neue Benutzeroberflächen Komponenten (Eigenschaften Seiten, Menü Elemente und Attribut anzeigen Amen) können hinzugefügt oder die vorhandene Benutzeroberfläche ersetzt werden. Es ist auch möglich, neue Eigenschaften Seiten zu entwerfen, die weniger Attribute einer Klasse verfügbar machen und Kontextmenüs mit weniger Aktionen erstellen. Weitere Informationen finden Sie unter [Eigenschaften Seiten für die Verwendung mit Anzeige Spezifizierer](property-pages-for-use-with-display-specifiers.md), [Kontextmenüs für die Verwendung mit Anzeige Spezifizierer](context-menus-for-use-with-display-specifiers.md)und [Klassen-und Attribut anzeigen Amen](class-and-attribute-display-names.md).

 

 





