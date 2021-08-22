---
title: Festlegen von Rechten auf bestimmte Eigenschaften bestimmter Objekttypen
description: Eigenschaftenspezifische Berechtigungen können in Kombination mit objektspezifischer Vererbung verwendet werden, um eine leistungsstarke und detaillierte Delegierung der Verwaltung zu ermöglichen.
ms.assetid: d2ebbe3a-78f7-4bb5-bac0-13236031b7b1
ms.tgt_platform: multiple
keywords:
- Festlegen von Rechten auf bestimmte Eigenschaften bestimmter Objekttypen AD
- Active Directory, Verwenden, Sicherheit, Festlegen von Rechten auf bestimmte Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c01070b5c5b23e7524bd3b54293576e578861e0120b431e6dc95b7a5b4cc4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024738"
---
# <a name="setting-rights-to-specific-properties-of-specific-types-of-objects"></a>Festlegen von Rechten auf bestimmte Eigenschaften bestimmter Objekttypen

Eigenschaftenspezifische Berechtigungen können in Kombination mit objektspezifischer Vererbung verwendet werden, um eine leistungsstarke und detaillierte Delegierung der Verwaltung zu ermöglichen. Sie können einen eigenschaftenspezifischen objektvererbbaren ACE festlegen, damit ein angegebener Benutzer oder eine angegebene Gruppe ein bestimmtes Attribut in einer angegebenen Klasse untergeordneter Objekte in einem Container lesen und/oder schreiben kann. Beispielsweise können Sie einen ACE für eine Organisationseinheit (OU) festlegen, um einer Gruppe das Lesen und Schreiben des Telefonnummernattributs aller Benutzerobjekte in der Organisationseinheit zu ermöglichen.

**So legen Sie eigenschaftenspezifische objektvererbbare ACEs fest**

1.  Legen [**Sie IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS \_ ACETYPE ACCESS ALLOWED \_ \_ \_ OBJECT** oder **ADS \_ ACETYPE ACCESS \_ \_ DENIED OBJECT \_ fest.**
2.  Legen [**Sie IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **schemaIDGUID** des Attributs fest. Beispielsweise ist **die schemaIDGUID** des **telephoneNumber-Attributs** {bf967a49-0de6-11d0-a285-00aa003049e2}.
3.  Legen [**Sie IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS \_ ACEFLAG \_ INHERIT ACE \_ fest.**
4.  Legen [**Sie IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **die schemaIDGUID** der Objektklasse fest, die den ACE erben kann. Beispielsweise ist **die schemaIDGUID** der Benutzerklasse {bf967aba-0de6-11d0-a285-00aa003049e2}. 
5.  Legen [**Sie IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS FLAG OBJECT TYPE \_ \_ \_ \_ PRESENT** und **ADS FLAG \_ \_ INHERITED OBJECT TYPE PRESENT \_ \_ \_ fest.**

> [!IMPORTANT]
> Legen Sie ADS \_ ACEFLAG \_ INHERIT \_ ACE fest, damit der ACE geerbt wird. Legen Sie darüber hinaus ADS ACEFLAG INHERIT ONLY ACE fest, wenn der Objekttyp, für den dieser ACE gilt, nicht mit dem Objekttyp des Containers, in dem der ACE angegeben ist, \_ \_ \_ \_ übereintrifft. Wenn dies nicht erfolgt, wird der ACE auch für den Container wirksam und kann unerwartete Rechte gewähren.

 

Weitere Informationen und Codebeispiele, die zum Festlegen dieser Art von ACE verwendet werden können, finden Sie unter Beispielcode für das Festlegen eines [ACE für ein Verzeichnisobjekt.](example-code-for-setting-an-ace-on-a-directory-object.md)

 

 