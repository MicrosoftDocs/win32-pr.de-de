---
title: Statusanzeige-Steuer Element (MSAA-Benutzeroberflächen-Element Referenz)
description: Statusanzeige-Steuerelemente zeigen den Fortschritt eines langwierigen Vorgangs an, z. b. das Herunterladen einer Datei aus dem Internet. Der Fortschritt wird in der Regel als Prozentsatz zwischen NULL (0) und 100 (100) ausgedrückt.
ms.assetid: 9165d00e-b3f3-41cd-812c-cd39313460fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9bbd9a648ee1c4d4f112577c8e41a5983f69038
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207128"
---
# <a name="progress-bar-control-msaa-ui-element-reference"></a>Statusanzeige-Steuer Element (MSAA-Benutzeroberflächen-Element Referenz)

> [!Note]  
> In diesem Thema werden Statusanzeige- **Steuer** Element Objekte zum Zweck der MSAA-Benutzeroberflächen-Element Referenz beschrieben. Das Erstellen von **Status** Anzeige-Steuerelement Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Statusanzeige-Steuerelemente zeigen den Fortschritt eines langwierigen Vorgangs an, z. b. das Herunterladen einer Datei aus dem Internet. Der Fortschritt wird in der Regel als Prozentsatz zwischen NULL (0) und 100 (100) ausgedrückt.

Der Fenster Klassenname für ein Statusanzeige-Steuerelement ist \_ "Progress Class", das in "commctrl. h" als "msctls \_ Progress" definiert ist.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Die Statusanzeige-Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Die Statusanzeige-Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **childCount** -Eigenschaft ist 0 (null).                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_accKeyboardShortcut erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut** -Eigenschaft ist die Zugriffstaste der Statusanzeige, bei der es sich um ein unterstrichenes Zeichen im Text der Bezeichnung für die Statusanzeige handelt. Die zurückgegebene Zeichenfolge enthält das Zugriffsschlüssel Zeichen, das an die Zeichenfolge "alt +" angehängt wird.                                                                                                                                                                                                                                 |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name** -Eigenschaft ist der Text aus einem statischen Text Steuerelement, das die Statusanzeige bezeichnet.                                                                                                                                                                                                                                                                                                                                                                               |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die gleiche **Name** -Eigenschaft und den Fenster Klassennamen wie das Steuerelement aufweist.                                                                                                                                                                                                                                                              |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role** -Eigenschaft ist [**role \_ System \_ ProgressBar**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                      |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |
| [**\_accValue erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | Die **value** -Eigenschaft ist eine Zeichenfolge von "0%" bis "100%", die den Fortschritt beschreibt.                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





