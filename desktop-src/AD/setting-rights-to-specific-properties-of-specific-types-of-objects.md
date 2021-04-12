---
title: Festlegen von Rechten auf bestimmte Eigenschaften bestimmter Objekttypen
description: Eigenschaften spezifische Berechtigungen können in Kombination mit Objekt spezifischer Vererbung verwendet werden, um die leistungsstarke und detaillierte Delegierung der Verwaltung bereitzustellen.
ms.assetid: d2ebbe3a-78f7-4bb5-bac0-13236031b7b1
ms.tgt_platform: multiple
keywords:
- Festlegen von Rechten auf bestimmte Eigenschaften bestimmter Objekttypen (AD)
- Active Directory, verwenden von, Sicherheit, Festlegen von Rechten auf bestimmte Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79bfa24b574639e64fbb17c33fabee1185cc014c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472460"
---
# <a name="setting-rights-to-specific-properties-of-specific-types-of-objects"></a>Festlegen von Rechten auf bestimmte Eigenschaften bestimmter Objekttypen

Eigenschaften spezifische Berechtigungen können in Kombination mit Objekt spezifischer Vererbung verwendet werden, um die leistungsstarke und detaillierte Delegierung der Verwaltung bereitzustellen. Sie können einen Eigenschafts spezifischen Objekt-vererbbaren ACE festlegen, um einem bestimmten Benutzer oder einer Gruppe das Lesen und/oder Schreiben eines bestimmten Attributs für eine bestimmte Klasse von untergeordneten Objekten in einem Container zu ermöglichen. Beispielsweise können Sie einen ACE für eine Organisationseinheit festlegen, um einer Gruppe das Lesen und Schreiben des telefonnummerattributs für alle Benutzer Objekte in der Organisationseinheit zu ermöglichen.

**So legen Sie Eigenschaften spezifische, Objekt vererbbare ACEs fest**

1.  Legen Sie [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf ADS für den Zugriff auf das Objekt " **\_ \_ Zugriff \_ zugelassen \_** " oder " **AD \_ AceType \_ Access \_ denied \_**" fest.
2.  Legen Sie [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf die **schemaIdGUID** des Attributs fest. Die **schemaIdGUID** des **telefonienumber** -Attributs lautet beispielsweise {bf967a49-0de6-11D0-A285-00aa003049e2}.
3.  Legen Sie [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS \_ aceflag \_ erbt \_ ACE** fest.
4.  Legen Sie [**IADsAccessControlEntry. eritedobjecttype**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf die **schemaIdGUID** der Objektklasse fest, die den ACE erben kann. Die **schemaIdGUID** der **Benutzer** Klasse lautet beispielsweise {bf967aba-0de6-11D0-A285-00aa003049e2}.
5.  Legen Sie [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS-Flag- \_ \_ \_ Objekttyp \_ vorhanden** und **Anzeigen der \_ \_ geerbten \_ \_ Objekttyp \_ vorhanden** fest.

> [!IMPORTANT]
> Legen \_ \_ Sie fest \_ , dass die ACE-Zugriffs Steuerungs Liste den ACE erben soll. Außerdem wird durch Set ADS \_ aceflag \_ \_ nur ACE geerbt, \_ Wenn der Objekttyp, auf den dieser ACE angewendet wird, nicht mit dem Objekttyp des Containers identisch ist, in dem der ACE angegeben ist. Wenn dies nicht der Fall ist, wird der ACE auch für den Container wirksam und kann unerwartete Rechte erteilen.

 

Weitere Informationen und Codebeispiele, die verwendet werden können, um diese Art von ACE festzulegen, finden Sie unter [Beispielcode für das Festlegen eines ACE für ein Verzeichnis Objekt](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 