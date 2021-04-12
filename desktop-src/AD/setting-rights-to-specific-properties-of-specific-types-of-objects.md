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
# <a name="setting-rights-to-specific-properties-of-specific-types-of-objects"></a><span data-ttu-id="eda97-105">Festlegen von Rechten auf bestimmte Eigenschaften bestimmter Objekttypen</span><span class="sxs-lookup"><span data-stu-id="eda97-105">Setting Rights to Specific Properties of Specific Types of Objects</span></span>

<span data-ttu-id="eda97-106">Eigenschaften spezifische Berechtigungen können in Kombination mit Objekt spezifischer Vererbung verwendet werden, um die leistungsstarke und detaillierte Delegierung der Verwaltung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eda97-106">Property-specific permissions can be used in combination with object specific inheritance to provide the powerful and detailed delegation of administration.</span></span> <span data-ttu-id="eda97-107">Sie können einen Eigenschafts spezifischen Objekt-vererbbaren ACE festlegen, um einem bestimmten Benutzer oder einer Gruppe das Lesen und/oder Schreiben eines bestimmten Attributs für eine bestimmte Klasse von untergeordneten Objekten in einem Container zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="eda97-107">You can set a property-specific object-inheritable ACE to allow a specified user or group to read and/or write a specific attribute on a specified class of child objects in a container.</span></span> <span data-ttu-id="eda97-108">Beispielsweise können Sie einen ACE für eine Organisationseinheit festlegen, um einer Gruppe das Lesen und Schreiben des telefonnummerattributs für alle Benutzer Objekte in der Organisationseinheit zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="eda97-108">For example, you can set an ACE on an organizational unit (OU) to enable a group to read and write the telephone number attribute of all user objects in the OU.</span></span>

<span data-ttu-id="eda97-109">**So legen Sie Eigenschaften spezifische, Objekt vererbbare ACEs fest**</span><span class="sxs-lookup"><span data-stu-id="eda97-109">**To set property-specific object-inheritable ACEs**</span></span>

1.  <span data-ttu-id="eda97-110">Legen Sie [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf ADS für den Zugriff auf das Objekt " **\_ \_ Zugriff \_ zugelassen \_** " oder " **AD \_ AceType \_ Access \_ denied \_**" fest.</span><span class="sxs-lookup"><span data-stu-id="eda97-110">Set [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="eda97-111">Legen Sie [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf die **schemaIdGUID** des Attributs fest.</span><span class="sxs-lookup"><span data-stu-id="eda97-111">Set [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to the **schemaIDGUID** of the attribute.</span></span> <span data-ttu-id="eda97-112">Die **schemaIdGUID** des **telefonienumber** -Attributs lautet beispielsweise {bf967a49-0de6-11D0-A285-00aa003049e2}.</span><span class="sxs-lookup"><span data-stu-id="eda97-112">For example, the **schemaIDGUID** of the **telephoneNumber** attribute is {bf967a49-0de6-11d0-a285-00aa003049e2}.</span></span>
3.  <span data-ttu-id="eda97-113">Legen Sie [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS \_ aceflag \_ erbt \_ ACE** fest.</span><span class="sxs-lookup"><span data-stu-id="eda97-113">Set [**IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACEFLAG\_INHERIT\_ACE**.</span></span>
4.  <span data-ttu-id="eda97-114">Legen Sie [**IADsAccessControlEntry. eritedobjecttype**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf die **schemaIdGUID** der Objektklasse fest, die den ACE erben kann.</span><span class="sxs-lookup"><span data-stu-id="eda97-114">Set [**IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to the **schemaIDGUID** of the object class that can inherit the ACE.</span></span> <span data-ttu-id="eda97-115">Die **schemaIdGUID** der **Benutzer** Klasse lautet beispielsweise {bf967aba-0de6-11D0-A285-00aa003049e2}.</span><span class="sxs-lookup"><span data-stu-id="eda97-115">For example, the **schemaIDGUID** of the **user** class is {bf967aba-0de6-11d0-a285-00aa003049e2}.</span></span>
5.  <span data-ttu-id="eda97-116">Legen Sie [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS-Flag- \_ \_ \_ Objekttyp \_ vorhanden** und **Anzeigen der \_ \_ geerbten \_ \_ Objekttyp \_ vorhanden** fest.</span><span class="sxs-lookup"><span data-stu-id="eda97-116">Set [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT** and **ADS\_FLAG\_INHERITED\_OBJECT\_TYPE\_PRESENT**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eda97-117">Legen \_ \_ Sie fest \_ , dass die ACE-Zugriffs Steuerungs Liste den ACE erben soll.</span><span class="sxs-lookup"><span data-stu-id="eda97-117">Set ADS\_ACEFLAG\_INHERIT\_ACE to cause the ACE to be inherited.</span></span> <span data-ttu-id="eda97-118">Außerdem wird durch Set ADS \_ aceflag \_ \_ nur ACE geerbt, \_ Wenn der Objekttyp, auf den dieser ACE angewendet wird, nicht mit dem Objekttyp des Containers identisch ist, in dem der ACE angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="eda97-118">In addition, set ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE if the object type this ACE applies to does not match the object type of the container where the ACE is specified.</span></span> <span data-ttu-id="eda97-119">Wenn dies nicht der Fall ist, wird der ACE auch für den Container wirksam und kann unerwartete Rechte erteilen.</span><span class="sxs-lookup"><span data-stu-id="eda97-119">If this is not done, the ACE will also become effective on the container and can grant unexpected rights.</span></span>

 

<span data-ttu-id="eda97-120">Weitere Informationen und Codebeispiele, die verwendet werden können, um diese Art von ACE festzulegen, finden Sie unter [Beispielcode für das Festlegen eines ACE für ein Verzeichnis Objekt](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="eda97-120">For more information and code examples that can be used to set this kind of ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 