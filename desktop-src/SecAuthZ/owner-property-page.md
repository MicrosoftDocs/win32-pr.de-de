---
description: Der Zugriffs Steuerungs-Editor kann eine Eigenschaften Seite des Besitzers enthalten, die es dem Benutzer ermöglicht, einen Objektbesitzer zu ändern. Weitere Informationen zu Objekt Besitzern finden Sie unter Besitzer eines neuen Objekts und Übernahme des Objekt Besitzes in C++.
ms.assetid: b0c421db-450e-4030-98e9-e062202e482c
title: Besitzer (Eigenschaften Seite)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee9d5c276071674ec274c9955a2e8c5cd5a856a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131929"
---
# <a name="owner-property-page"></a><span data-ttu-id="8c60e-104">Besitzer (Eigenschaften Seite)</span><span class="sxs-lookup"><span data-stu-id="8c60e-104">Owner Property Page</span></span>

<span data-ttu-id="8c60e-105">Der Zugriffs Steuerungs-Editor kann eine Eigenschaften Seite des Besitzers enthalten, die es dem Benutzer ermöglicht, den Besitzer eines Objekts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8c60e-105">The access control editor can include an Owner property page that enables the user to change an object's owner.</span></span> <span data-ttu-id="8c60e-106">Weitere Informationen zum Besitzer eines Objekts finden Sie unter [Besitzer eines neuen Objekts](owner-of-a-new-object.md) und Übernahme des [Objekt Besitzes in C++](taking-object-ownership-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="8c60e-106">For more information about an object's owner, see [Owner of a New Object](owner-of-a-new-object.md) and [Taking Object Ownership in C++](taking-object-ownership-in-c--.md).</span></span>

<span data-ttu-id="8c60e-107">Die Eigenschaften Seite **Besitzer** befindet sich auf der Eigenschaften Seite [Erweiterte Sicherheit](advanced-security-property-sheet.md) , die angezeigt wird, wenn der Benutzer auf der [Eigenschaften Seite grundlegende Sicherheit](basic-security-property-page.md)auf die Schaltfläche **erweitert** klickt.</span><span class="sxs-lookup"><span data-stu-id="8c60e-107">The **Owner** property page is in the [advanced security property sheet](advanced-security-property-sheet.md) displayed when the user clicks the **Advanced** button on the [basic security property page](basic-security-property-page.md).</span></span> <span data-ttu-id="8c60e-108">Legen Sie die  Eigenschaft Si \_ Advanced und Si \_ Edit \_ owner in der [**Si \_ Object \_ Info**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) -Struktur fest, die von Ihrer [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) -Implementierung zurückgegeben wird, um die Eigenschaften Seite "Owner" einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="8c60e-108">To include the **Owner** property page, set the SI\_ADVANCED and SI\_EDIT\_OWNER flags in the [**SI\_OBJECT\_INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) implementation.</span></span>

 

 
