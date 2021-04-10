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
# <a name="deleting-a-class-or-instance"></a>Löschen einer Klasse oder Instanz

Wenn Sie mit einer Klasse oder einer Instanz fertig sind, möchten Sie möglicherweise die Klasse oder Instanz aus WMI löschen. Wie bei anderen objektorientierten Technologien können Sie Klassen-oder Instanzobjekte löschen, um den WMI-Namespace zu bereinigen und Systemressourcen zurückzugeben. Viele Klassen und Instanzen in WMI sind jedoch persistent und werden von einer Vielzahl von Anwendungen zu einem beliebigen Zeitpunkt verwendet. Daher sollten Sie beim Löschen einer WMI-Klasse oder-Instanz sorgfältig vorgehen: Ihre Anwendung oder eine andere Anwendung benötigt wahrscheinlich die Klasse oder Instanz zu einem späteren Zeitpunkt.

Das Löschen einer Klasse oder einer Instanz ist eine einfache Prozedur. Aufgrund der permanenten Natur einer Klasse ist es jedoch wahrscheinlich nicht erforderlich, eine Klasse häufig zu löschen. Beispielsweise ist es unwahrscheinlich, dass Sie die [**Win32 \_ diskdrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) -Klasse löschen, da es unwahrscheinlich ist, dass Sie in Ihrem Unternehmen nicht über ein Festplattenlaufwerk verfügen. Stattdessen wird es wahrscheinlicher, dass Sie eine Instanz einer Klasse löschen. Weitere Informationen finden Sie unter [Löschen einer Instanz](deleting-an-instance.md).

Obwohl es ungewöhnlich ist, kann es sein, dass Sie eine von Ihnen erstellte Klasse aktualisieren möchten. Beispielsweise können Sie eine Klasse erstellen, die eine Drittanbieter Anwendung darstellt. Wenn der Drittanbieter seine Software so aktualisiert hat, dass die-Klasse die Software nicht mehr ordnungsgemäß darstellt, müssen Sie möglicherweise die ursprüngliche Klasse löschen. Weitere Informationen finden Sie unter [Löschen einer Klasse](deleting-a-class.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
