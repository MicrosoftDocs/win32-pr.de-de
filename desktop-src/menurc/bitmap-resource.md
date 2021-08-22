---
title: BITMAP-Ressource
description: Definiert eine Bitmap, die eine Anwendung in der Bildschirmanzeige oder als Element in einem Menü oder Steuerelement verwendet.
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- BITMAP-Ressourcenmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff75f235e8aa1787e93f9420b4d7ed27f440cdc09510547295ebced4ec494bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734898"
---
# <a name="bitmap-resource"></a>BITMAP-Ressource

Definiert eine Bitmap, die eine Anwendung in der Bildschirmanzeige oder als Element in einem Menü oder Steuerelement verwendet.

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Eindeutiger Name oder ein 16-Bit-Ganzzahlwert ohne Vorzeichen, der die Ressource identifiziert.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Dateiname*
</dt> <dd>

Name der Datei, die die Ressource enthält. Der Name muss ein gültiger Dateiname sein. es muss ein vollständiger Pfad sein, wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet. Der Pfad sollte eine Zeichenfolge in Anführungs zeichen sein.

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [Allgemeine Ressourcenattribute.](common-resource-attributes.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel werden zwei Bitmapressourcen definiert:

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Verwenden von Bitmaps](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[**Loadimage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 