---
title: Bitmap-Ressource
description: Definiert eine Bitmap, die von einer Anwendung in der Bildschirm Anzeige oder als Element in einem Menü oder Steuerelement verwendet wird.
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- Bitmap-Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5bed33fb66d9deb85e1f25165f3f7a0f664961
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390211"
---
# <a name="bitmap-resource"></a>Bitmap-Ressource

Definiert eine Bitmap, die von einer Anwendung in der Bildschirm Anzeige oder als Element in einem Menü oder Steuerelement verwendet wird.

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*
</dt> <dd>

Eindeutiger Name oder ein 16-Bit-Ganzzahl-Wert ohne Vorzeichen, der die Ressource identifiziert.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Einfügen*
</dt> <dd>

Der Name der Datei, die die Ressource enthält. Der Name muss ein gültiger Dateiname sein. Es muss sich um einen vollständigen Pfad handeln, wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet. Der Pfad muss eine Zeichenfolge in Anführungszeichen sein.

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel werden zwei Bitmapressourcen definiert:

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Bitmaps](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 