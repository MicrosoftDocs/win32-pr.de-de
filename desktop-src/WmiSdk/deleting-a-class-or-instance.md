---
description: Wenn Sie mit einer Klasse oder einer Instanz fertig sind, möchten Sie möglicherweise die Klasse oder Instanz aus WMI löschen.
ms.assetid: 8d4bf548-a332-4058-92d0-d613bbeaa408
ms.tgt_platform: multiple
title: Löschen einer Klasse oder Instanz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a46a52400623e31df3e051a0b587f49326733b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215456"
---
# <a name="deleting-a-class-or-instance"></a><span data-ttu-id="f2bd3-103">Löschen einer Klasse oder Instanz</span><span class="sxs-lookup"><span data-stu-id="f2bd3-103">Deleting a Class or Instance</span></span>

<span data-ttu-id="f2bd3-104">Wenn Sie mit einer Klasse oder einer Instanz fertig sind, möchten Sie möglicherweise die Klasse oder Instanz aus WMI löschen.</span><span class="sxs-lookup"><span data-stu-id="f2bd3-104">After you finish with a class or an instance, you may wish to delete that class or instance from WMI.</span></span> <span data-ttu-id="f2bd3-105">Wie bei anderen objektorientierten Technologien können Sie Klassen-oder Instanzobjekte löschen, um den WMI-Namespace zu bereinigen und Systemressourcen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="f2bd3-105">Like other object-oriented technologies, you can delete class or instance objects to clean up the WMI namespace and to return system resources.</span></span> <span data-ttu-id="f2bd3-106">Viele Klassen und Instanzen in WMI sind jedoch persistent und werden von einer Vielzahl von Anwendungen zu einem beliebigen Zeitpunkt verwendet. Daher sollten Sie beim Löschen einer WMI-Klasse oder-Instanz sorgfältig vorgehen: Ihre Anwendung oder eine andere Anwendung benötigt wahrscheinlich die Klasse oder Instanz zu einem späteren Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="f2bd3-106">However, many classes and instances in WMI are persistent and are used by a variety of applications at any given time Therefore, you should be careful when deleting a WMI class or instance: your application or another application will probably need the class or instance at a later date.</span></span>

<span data-ttu-id="f2bd3-107">Das Löschen einer Klasse oder einer Instanz ist eine einfache Prozedur.</span><span class="sxs-lookup"><span data-stu-id="f2bd3-107">Deleting a class or an instance is a simple procedure.</span></span> <span data-ttu-id="f2bd3-108">Aufgrund der permanenten Natur einer Klasse ist es jedoch wahrscheinlich nicht erforderlich, eine Klasse häufig zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f2bd3-108">However, due to the permanent nature of a class, you will probably not need to delete a class often.</span></span> <span data-ttu-id="f2bd3-109">Beispielsweise ist es unwahrscheinlich, dass Sie die [**Win32 \_ diskdrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) -Klasse löschen, da es unwahrscheinlich ist, dass Sie in Ihrem Unternehmen nicht über ein Festplattenlaufwerk verfügen.</span><span class="sxs-lookup"><span data-stu-id="f2bd3-109">For example, you are unlikely to delete the [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) class, because it is unlikely that you do not have a disk drive somewhere in your enterprise.</span></span> <span data-ttu-id="f2bd3-110">Stattdessen wird es wahrscheinlicher, dass Sie eine Instanz einer Klasse löschen.</span><span class="sxs-lookup"><span data-stu-id="f2bd3-110">Instead, you will be more likely to delete an instance of a class.</span></span> <span data-ttu-id="f2bd3-111">Weitere Informationen finden Sie unter [Löschen einer Instanz](deleting-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="f2bd3-111">For more information, see [Deleting an Instance](deleting-an-instance.md).</span></span>

<span data-ttu-id="f2bd3-112">Obwohl es ungewöhnlich ist, kann es sein, dass Sie eine von Ihnen erstellte Klasse aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f2bd3-112">Although uncommon, you may come across a time where you wish to update a class that you created.</span></span> <span data-ttu-id="f2bd3-113">Beispielsweise können Sie eine Klasse erstellen, die eine Drittanbieter Anwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="f2bd3-113">For example, you could create a class to represent a third-party application.</span></span> <span data-ttu-id="f2bd3-114">Wenn der Drittanbieter seine Software so aktualisiert hat, dass die-Klasse die Software nicht mehr ordnungsgemäß darstellt, müssen Sie möglicherweise die ursprüngliche Klasse löschen.</span><span class="sxs-lookup"><span data-stu-id="f2bd3-114">If the third-party updated their software to the extent that your class no longer properly represented the software, you may need to delete your original class.</span></span> <span data-ttu-id="f2bd3-115">Weitere Informationen finden Sie unter [Löschen einer Klasse](deleting-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="f2bd3-115">For more information, see [Deleting a Class](deleting-a-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2bd3-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2bd3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2bd3-117">Entwerfen von Managed Object Format-Klassen (MOF)</span><span class="sxs-lookup"><span data-stu-id="f2bd3-117">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
