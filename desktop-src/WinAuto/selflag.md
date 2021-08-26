---
title: SELFLAG-Konstanten (Oleacc.h)
description: In diesem Thema werden die konstanten Werte beschrieben, mit denen angegeben wird, wie ein barrierefreies Objekt ausgewählt wird oder den Fokus erhält.
ms.assetid: 52755540-dcf4-4e0b-bb5c-88b05f134d79
topic_type:
- apiref
api_name:
- SELFLAG_NONE
- SELFLAG_TAKEFOCUS
- SELFLAG_TAKESELECTION
- SELFLAG_EXTENDSELECTION
- SELFLAG_ADDSELECTION
- SELFLAG_REMOVESELECTION
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b4d0384b66919a55d55593d2e16c9a187d84ac
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478581"
---
# <a name="selflag-constants"></a>SELFLAG-Konstanten

In diesem Thema werden die konstanten Werte beschrieben, mit denen angegeben wird, wie ein barrierefreies Objekt ausgewählt wird oder den Fokus erhält. Die Konstanten werden in oleacc.h definiert und mit der [**IAccessible::accSelect-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) verwendet.

Die folgenden Kombinationen sind nicht zulässig:

-   SELFLAG \_ ADDSELECTION \| SELFLAG \_ REMOVESELECTION
-   SELFLAG \_ ADDSELECTION \| SELFLAG \_ TAKESELECTION
-   SELFLAG \_ REMOVESELECTION \| SELFLAG \_ TAKESELECTION
-   SELFLAG \_ EXTENDSELECTION \| SELFLAG \_ TAKESELECTION

**Hinweis für Clients:** Microsoft Active Accessibility unterstützt nicht die Auswahl des Texts, der in Bearbeitungs- und Rich Edit-Steuerelementen enthalten ist, da der Text als Zeichenfolge in der [Value-Eigenschaft](value-property.md)des Objekts verfügbar gemacht wird.

Informationen zum Ausführen komplexer Auswahlvorgänge finden Sie unter [Auswählen von untergeordneten Objekten.](selecting-child-objects.md)




| Konstante/Wert | BESCHREIBUNG | 
|----------------|-------------|
| <span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl><dt><strong>SELFLAG_NONE</strong></dt><dt>0</dt></dl> | Führt keine Aktion aus. Microsoft Active Accessibility ändert die Auswahl oder den Fokus nicht.<br /> | 
| <span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl><dt><strong>SELFLAG_TAKEFOCUS</strong></dt><dt>0x1</dt></dl> | Legt den Fokus auf das Objekt fest und legt es als Auswahlanker fest. Dieses Flag wird allein verwendet und ändert die Auswahl nicht. Der Effekt ähnelt dem manuellen Verschieben des Fokus durch Drücken einer PFEILTASTE, während Sie die STRG-TASTE im Windows Explorer oder in einem beliebigen Listenfeld mit mehrfacher Auswahl gedrückt halten. <br /> Bei -Objekten mit dem <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>wird SELFLAG_TAKEFOCUS mit den folgenden Werten kombiniert:<br /><ul><li>SELFLAG_TAKESELECTION</li><li>SELFLAG_EXTENDSELECTION</li><li>SELFLAG_ADDSELECTION</li><li>SELFLAG_REMOVESELECTION</li><li>SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</li><li>SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</li></ul>Wenn Sie <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible::accSelect</strong></a> mit dem flag SELFLAG_TAKEFOCUS für ein Objekt aufrufen, das über ein <strong>HWND</strong>verfügt, wird das Flag nur wirksam, wenn das übergeordnete Element des Objekts bereits den Fokus besitzt.<br /> | 
| <span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl><dt><strong>SELFLAG_TAKESELECTION</strong></dt><dt>0x2</dt></dl> | Wählt das -Objekt aus und entfernt die Auswahl aus allen anderen Objekten im Container. <br /> Dieses Flag ändert weder den Fokus noch den Auswahlanker, es sei denn, es wird mit SELFLAG_TAKEFOCUS kombiniert. Die SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS Kombination entspricht dem Einfachklick auf ein Element in Windows Explorer.<br /> Dieses Flag darf nicht mit den folgenden Flags kombiniert werden:<br /><ul><li>SELFLAG_ADDSELECTION</li><li>SELFLAG_REMOVESELECTION</li><li>SELFLAG_EXTENDSELECTION</li></ul> | 
| <span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt><dt>0x4</dt></dl> | Ändert die Auswahl so, dass alle Objekte zwischen dem Auswahlanker und diesem Objekt den Auswahlzustand des Ankerobjekts übernehmen. Wenn das Ankerobjekt nicht ausgewählt ist, werden die Objekte aus der Auswahl entfernt. Wenn das Ankerobjekt ausgewählt ist, wird die Auswahl erweitert, um dieses Objekt und alle dazwischen enthaltenen Objekte einzuschließt. Legen Sie den Auswahlzustand fest, indem Sie dieses Flag mit SELFLAG_ADDSELECTION oder SELFLAG_REMOVESELECTION kombinieren. <br /> Dieses Flag ändert weder den Fokus noch den Auswahlanker, es sei denn, es wird mit SELFLAG_TAKEFOCUS kombiniert. Die SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS Kombination entspricht dem manuellen Hinzufügen eines Elements zu einer Auswahl, indem sie die UMSCHALTTASTE gedrückt hält und auf ein nicht ausgewähltes Objekt in Windows Explorer klickt.<br /> Dieses Flag wird nicht mit SELFLAG_TAKESELECTION kombiniert.<br /> | 
| <span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl><dt><strong>SELFLAG_ADDSELECTION</strong></dt><dt>0x8</dt></dl> | Fügt der aktuellen Auswahl das -Objekt hinzu. Mögliches Ergebnis ist eine nicht zusammenhängende Auswahl. <br /> Dieses Flag ändert weder den Fokus noch den Auswahlanker, es sei denn, es wird mit SELFLAG_TAKEFOCUS kombiniert. Die SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS Kombination entspricht dem manuellen Hinzufügen eines Elements zu einer Auswahl, indem sie die STRG-TASTE gedrückt hält und auf ein nicht ausgewähltes Objekt in Windows Explorer klickt.<br /> Dieses Flag wird nicht mit SELFLAG_REMOVESELECTION oder SELFLAG_TAKESELECTION kombiniert.<br /> | 
| <span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl><dt><strong>SELFLAG_REMOVESELECTION</strong></dt><dt>0x10</dt></dl> | Entfernt das -Objekt aus der aktuellen Auswahl. Mögliches Ergebnis ist eine nicht zusammenhängende Auswahl. <br /> Dieses Flag ändert weder den Fokus noch den Auswahlanker, es sei denn, es wird mit SELFLAG_TAKEFOCUS kombiniert. Die SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS Kombination entspricht dem manuellen Entfernen eines Elements aus einer Auswahl, indem die STRG-TASTE gedrückt gehalten wird, während sie auf ein ausgewähltes Objekt in Windows Explorer klickt.<br /> Dieses Flag wird nicht mit SELFLAG_ADDSELECTION oder SELFLAG_TAKESELECTION kombiniert.<br /> | 




## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Oleacc.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[Auswählen von untergeordneten Objekten](selecting-child-objects.md)
</dt> </dl>

 

 





