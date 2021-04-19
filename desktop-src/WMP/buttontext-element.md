---
title: ButtonText-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | ButtonText-Element
ms.assetid: 1afe1626-769a-40c8-883a-968ebd995a93
keywords:
- Fenster "ButtonText-Element" Media Player
topic_type:
- apiref
api_name:
- ButtonText Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c94577ad772a5c6fa198bd43f2475d53821da72c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369303"
---
# <a name="buttontext-element"></a>ButtonText-Element

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **ButtonText** -Element gibt die Text Zeichenfolge an, die Windows Media Player für eine Aufgabenbereichs Schaltfläche anzeigt.

``` syntax
<ButtonText>
   text string
</ButtonText>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Element                                              |
|-----------------|------------------------------------------------------|
| Übergeordnete Elemente | **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |
| Untergeordnete Elemente  | Keine                                                 |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element ist für jede Instanz von **ServiceTask1**, **ServiceTask2** oder **ServiceTask3** erforderlich.

> [!Note]  
> Windows Media Player 10 umfasst drei Aufgabenbereiche, in denen ein Online Shop seine Webseiten anzeigen kann. Der Online Shop kann einen, zwei oder alle drei Aufgabenbereiche verwenden. Windows Media Player 11 verfügt nur über einen Aufgabenbereich, den der Benutzer durch Klicken auf die Registerkarte " **Online Stores** " anzeigen kann. die **ServiceTask2** -und **ServiceTask3** -Elemente werden von Windows Media Player 11 ignoriert.

 

Windows Media Player kann den Text der Schaltfläche an den verfügbaren Platz anpassen. Der Player verwendet immer die "Tahoma Bold"-Schriftart mit 8 Punkten für diesen Text. Es stehen zwei Zeilen zum Anzeigen von Schaltflächen Text zur Verfügung, der Spieler umschließt jedoch nicht automatisch den Text von der ersten Zeile zum zweiten. Wenn Sie einen Zeilenumbruch im Schaltflächen Text angeben möchten, fügen Sie die neue Zeilen-Escapesequenz " \\ n" in die Text Zeichenfolge ein.

Die Text Zeichenfolge wird auch im Menü "Gehe **zu** " in der Windows Media Player-Benutzeroberfläche angezeigt.

Sie sollten Ihren Online Shop mithilfe verschiedener Anzeigeeinstellungen testen, um sicherzustellen, dass der Text erwartungsgemäß angezeigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





