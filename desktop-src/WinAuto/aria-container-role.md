---
title: ARIA-Containerrollenfehler
description: ARIA-Containerrollenfehler
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- AriaContainerRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507f094a5f7270565de0426b50afd6aef699607d857ef1ba7ed3d6c8bb1a1a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759830"
---
# <a name="aria-container-role-error"></a>ARIA-Containerrollenfehler

## <a name="text"></a>Text

Das Element mit **definierten Aktiv-Nachfolger-Elementen** verfügt nicht über eine Containerrolle (**Kombinationsfeld,** **Raster,** **Listenfeld,** **Menü,** **Menüleiste**, **Optionsgruppe**, **Struktur**, **Treegrid**, **Tablist**, **Zeile**).

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Dieser Fehler gilt für Elemente mit dem **Attribut aria-activedescendant.**

Ein Element scheint ein Container zu sein, für den das **aria-activedescendant-Attribut** festgelegt ist, aber das Rollenattribut des Elements verfügt nicht über einen Wert, der für einen Container gültig ist.

Um diesen Fehler zu beheben, legen Sie das **Rollenattribut** auf den Rollenwert Web Accessibility Initiative – Accessible Rich Internet Applications (CSV-ARIA) fest, der für ein Containerelement gültig ist: **Combobox,** **Raster,** **Listenfeld,** **Menü,** **Menüleiste,** **Optionsgruppe,** **Registerkartenliste,** **Struktur** oder **Treegrid**.

## <a name="example"></a>Beispiel


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1">
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ARIA-Rollenfehler](aria-role-invalid.md)
</dt> </dl>

 

 




