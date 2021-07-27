---
description: Eine weitere Option zum Hinzufügen von Verben zu einem kaskadierenden Menü ist IExplorerCommand::EnumSubCommands.
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed12cf78dc4b5f6a77bbd00b06897b49474a401
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436095"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a>Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle

Eine weitere Option zum Hinzufügen von Verben zu einem kaskadierenden Menü ist [**über IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Mit dieser Methode können Datenquellen, die ihre Befehlsmodulbefehle über die [**IExplorerCommandProvider-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) bereitstellen, diese Befehle als Verben in einem Kontextmenü verwenden. In Windows 7 und höher können Sie mithilfe der [**IExplorerCommand-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) die gleiche Verbimplementierung bereitstellen wie mit der [**IContextMenu-Schnittstelle.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)

## <a name="instructions"></a>Anweisungen


Die folgenden beiden Screenshots veranschaulichen die Verwendung von kaskadierenden Menüs im **Ordner Geräte.**

![Screenshot: Beispiel für ein kaskadiertes Menü im Ordner "devices"](images/file-assoc/FileCascadeMenu.png)

![Screenshot: Beispiel für ein kaskadiertes Menü im Ordner "devices"](images/file-assoc/cascadeDevices2.png)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Da [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) nur die In-Process-Aktivierung unterstützt, wird sie für die Verwendung durch Shell-Datenquellen empfohlen, die die Implementierung zwischen Befehlen und Kontextmenüs gemeinsam nutzen müssen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
