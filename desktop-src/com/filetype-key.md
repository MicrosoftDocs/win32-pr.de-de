---
title: Filetype-Schlüssel
description: Wird von getclassfile verwendet, um Muster mit verschiedenen Datei Bytes in einer nicht Verbund Datei abzugleichen.
ms.assetid: ced23cdb-c184-43fe-ba37-fe1af8664b66
keywords:
- Registrierungsschlüssel für filetype com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2e331588b627ee5ce9a9c1b69631f1e8a1dbe4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037528"
---
# <a name="filetype-key"></a>Filetype-Schlüssel

Wird von [**getclassfile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) verwendet, um Muster mit verschiedenen Datei Bytes in einer nicht Verbund Datei abzugleichen.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\FileType
   {CLSID}
      n = offset, cb, mask, value
```

<dl> <dt>

<span id="offset"></span><span id="OFFSET"></span>*kompensieren*
</dt> <dd>

Bestimmt, wie weit vom Anfang oder Ende der Datei bis zum Beginn des Vergleichs begonnen werden soll. Wenn der Offset ein negativer Wert ist, beginnt der Vergleich am Ende der Datei abzüglich des Offset Werts. Der Offset Wert ist ein Dezimaltyp, sofern nicht "0x" vorangestellt ist.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*betrieben*
</dt> <dd>

Stellt die Länge in Bytes zwischen dem Anfang und dem Ende der Datei dar. Stellt den Byte Bereich in der Datei dar. Der *CB* -Wert ist eine Dezimalzahl, sofern nicht "0x" vorangestellt ist.

</dd> <dt>

<span id="mask"></span><span id="MASK"></span>*chel*
</dt> <dd>

Ein binärer Wert, der für die Maskierung verwendet wird, der mit einer logischen and-Operation ausgeführt wird, und der durch *Offset* und *CB* angegebene Byte Bereich. Wenn dieser Wert ausgelassen wird, werden die Bytes auf alle Bytes festgelegt. Dieser Wert ist immer hexadezimal.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Wert*
</dt> <dd>

Stellt das Muster dar, das mit einer Datei mit diesem Dateityp verglichen werden muss. Das Muster wird verwendet, um ein bekanntes Dateiformat ordnungsgemäß und nicht durch die Erweiterung zu identifizieren.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Einträge werden von der [**getclassfile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) -Funktion verwendet, um Muster mit verschiedenen Datei Bytes in einer nicht Verbund Datei abzugleichen. **Filetype** hat CLSID-Unterschlüssel, von denen jeder eine Reihe von unter Schlüsseln **0**, **1**, **2**, **3** hat. Diese Werte enthalten Muster, die die festgestellte CLSID ergeben, wenn eine Übereinstimmung vorliegt. Der Wert "0, 4, FFFFFFFF, ABCD1234" gibt z. b. an, dass die ersten 4 Bytes in dieser Reihenfolge ABCD1234 sein müssen. Der Wert "-4, 4, fefefefe" gibt an, dass die letzten vier Bytes in der Datei fefefefe sein müssen. Wenn beide Muster übereinstimmen, wird die CLSID zurückgegeben.

Der Schlüssel **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** entspricht dem Stamm Schlüssel der **HKEY- \_ Klassen \_** , der für die Kompatibilität mit früheren Versionen von com beibehalten wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**<Datei \_ Erweiterung>**](-file-extension--key.md)
</dt> <dt>

[**Getclassfile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




