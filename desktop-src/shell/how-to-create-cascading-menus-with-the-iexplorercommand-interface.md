---
description: 'Eine weitere Option zum Hinzufügen von Verben zu einem kaskadierenden Menü ist die Verwendung von IExplorerCommand:: enumsubcommands.'
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afb88a7ac04857ac64e79115a4e8984d325e47b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104570967"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a>Erstellen von kaskadierenden Menüs mit der IExplorerCommand-Schnittstelle

Eine weitere Option zum Hinzufügen von Verben zu einem kaskadierenden Menü ist die Verwendung von [**IExplorerCommand:: enumsubcommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Diese Methode ermöglicht Datenquellen, die ihre Befehls Modul Befehle über die [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) -Schnittstelle bereitstellen, diese Befehle als Verben in einem Kontextmenü zu verwenden. In Windows 7 und höher können Sie die gleiche Verb Implementierung mithilfe der [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) -Schnittstelle bereitstellen, wie Sie es mit der [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) -Schnittstelle erreichen können.

## <a name="instructions"></a>Instructions


Die folgenden beiden Screenshots veranschaulichen die Verwendung von kaskadierenden Menüs im Ordner " **Geräte** ".

![Screenshot, der ein Beispiel für ein kaskadieres Menü im Geräte Ordner anzeigt.](images/file-assoc/filecascademenu.png)

![Screenshot mit einem Beispiel für ein kaskadieres Menü im Geräte Ordner](images/file-assoc/cascadedevices2.png)

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Da [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) nur die Prozess interne Aktivierung unterstützt, empfiehlt es sich, von shelldatenquellen zu verwenden, die die Implementierung zwischen Befehlen und Kontextmenüs freigeben müssen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
