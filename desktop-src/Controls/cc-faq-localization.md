---
title: Lokalisierungsunterstützung für allgemeine Steuerelemente
description: In diesem Thema wird die Unterstützung für nationale Sprachen beschrieben, die in die allgemeinen Steuerelemente integriert sind.
ms.assetid: c5720198-9071-4213-8dad-50b4c015c5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ccc307defa687c8640425dd781660641fe78a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947509"
---
# <a name="localization-support-for-common-controls"></a>Lokalisierungsunterstützung für allgemeine Steuerelemente

In diesem Thema wird die Unterstützung für nationale Sprachen beschrieben, die in die allgemeinen Steuerelemente integriert sind. Die integrierte Unterstützung für nationale Sprachen vereinfacht die Implementierung lokalisierter Anwendungen.

Dieses Thema enthält folgende Abschnitte:

-   [Angeben einer Sprache für die allgemeinen Steuerelemente](#specifying-a-language-for-the-common-controls)
-   [Angeben einer Sprache für Steuerelemente in einem Dialog Feld](#specifying-a-language-for-controls-in-a-dialog-box)
-   [Zugehörige Themen](#related-topics)

## <a name="specifying-a-language-for-the-common-controls"></a>Angeben einer Sprache für die allgemeinen Steuerelemente

Wenn Sie eine Sprache für die allgemeinen Steuerelemente angeben möchten, die sich von der Systemsprache unterscheiden, wenden Sie sich an [**initmuilanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage). Die von dieser Funktion angegebene Sprache gilt nur für den Prozess, von dem die Funktion aufgerufen wird.

Um die Sprache zu bestimmen, die derzeit von den allgemeinen Steuerelementen verwendet wird, nennen Sie [**getmuilanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage). Er gibt den Wert zurück, der durch einen vorherigen [**initmuilanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage)-Rückruf festgelegt wurde. Die zurückgegebene Sprache ist die, die für den Prozess angegeben wurde, von dem Sie aufgerufen wird. Wenn **initmuilanguage** nicht aufgerufen wurde oder von einem anderen Prozess aufgerufen wurde, gibt **getmuilanguage** einen Standardwert zurück.

## <a name="specifying-a-language-for-controls-in-a-dialog-box"></a>Angeben einer Sprache für Steuerelemente in einem Dialog Feld

Im Gegensatz zu allgemeinen Steuerelementen wird die aktuelle Systemsprache von vordefinierten Steuerelementen wie Schaltflächen oder Bearbeitungs Feldern nicht standardmäßig verwendet. Das Native Schriftart Steuerelement ist ein unsichtbares Steuerelement, das im Hintergrund funktioniert, damit die vordefinierten Steuerelemente eines Dialog Felds die aktuelle Systemsprache anzeigen können.

Gehen Sie folgendermaßen vor, um das Native Schriftart Steuerelement zu verwenden.

1.  Initialisieren Sie das Native Schriftart Steuerelement durch Aufrufen von [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex). Legen Sie den **dwicc** -Member der [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) -Struktur, auf die von *lpinitctrls* verwiesen wird, auf die Klasse "ICC \_ nativefntctl" fest \_ .
2.  Fügen Sie dem Ressourcen Skript für das Dialogfeld das-Steuerelement hinzu. Legen Sie mindestens eines der folgenden stilflags fest, um anzugeben, welche Steuerelemente betroffen sind. 

    | Flag              | Gilt für:                                                                                                                                                                                                                                                       |
    |-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | NFS- \_ Bearbeitung         | Steuerelemente bearbeiten                                                                                                                                                                                                                                                    |
    | NFS \_ static       | Statische Steuerelemente                                                                                                                                                                                                                                                  |
    | NFS- \_ listcombo    | Listen-, ComboBox-, List-View-und ComboBoxEx-Steuerelemente                                                                                                                                                                                                               |
    | NFS- \_ Schaltfläche       | Schaltflächen-Steuerelemente                                                                                                                                                                                                                                                  |
    | \_alle NFS          | Alle Steuerelemente                                                                                                                                                                                                                                                     |
    | NFS \_ usefontassoc | Ostasiatische Plattform. Das-Steuerelement verwendet die Schriftart Zuordnungs Funktion, anstatt zur systemeigenen Schriftart zu wechseln. Alle anderen Plattformen ignorieren diese. Dies ist für Windows Vista veraltet und wird in COMCTL V6 nicht unterstützt. Dies ist in COMCTL V5 aus Legacy Gründen vorhanden. |

    

     

Im folgenden Beispiel wird veranschaulicht, wie einem Ressourcen Skript ein System eigenes Schriftart Steuerelement hinzugefügt wird. Dies bewirkt, dass die Steuerelemente bearbeiten, auflisten und Kombinations Feld des Dialog Felds Text mithilfe der aktuellen Systemsprache anzeigen.


```
CONTROL    "",-1,"NativeFontCtl",NFS_EDIT|NFS_LISTCOMBO,0,0,0,0
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu allgemeinen Steuerelementen](common-controls-intro.md)
</dt> </dl>

 

 




