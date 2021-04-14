---
title: Acceltableentry-Struktur
description: Beschreibt die Daten in einer einzelnen Zugriffstasten-Tabellen Ressource. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- Acceltableentry-Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- ACCELTABLEENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9ff12fe39f2ea54c90530133263bceb157d79dcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479083"
---
# <a name="acceltableentry-structure"></a>Acceltableentry-Struktur

Beschreibt die Daten in einer einzelnen Zugriffstasten-Tabellen Ressource. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD fFlags;
  WORD wAnsi;
  WORD wId;
  WORD padding;
} ACCELTABLEENTRY;
```



## <a name="members"></a>Member

<dl> <dt>

**fFlags**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Beschreibt die Eigenschaften der Tastatur Beschleunigung. Dieser Member kann einen oder mehrere der folgenden Werte aus "Winuser. h" aufweisen.



| Wert                                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> " <dt>**evirtkey**</dt> " <dt>true</dt> </dl>    | Die Zugriffstaste ist ein Code, der aus dem [virtuellen Schlüssel](/windows/desktop/inputdev/virtual-key-codes)besteht. Wenn dieses Flag nicht angegeben wird, wird davon ausgegangen, dass die Zugriffstaste einen ASCII-Zeichencode angibt. <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <dt>**Spnoinvert**</dt> <dt>0x02</dt> </dl> | Ein Menü Element in der Menüleiste wird nicht hervorgehoben, wenn eine Zugriffstaste verwendet wird. Dieses Attribut ist veraltet und wird nur aus Gründen der Abwärtskompatibilität mit Ressourcen Dateien, die für 16-Bit-Windows entwickelt wurden, beibehalten.<br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <dt>**F**</dt> -Taste <dt>0x04</dt> </dl>          | Die Zugriffstaste wird nur aktiviert, wenn der Benutzer die UMSCHALTTASTE drückt. Dieses Flag gilt nur für virtuelle Schlüssel. <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <dt>**Steuerelement**</dt> <dt>0x08</dt> </dl>    | Die Zugriffstaste wird nur aktiviert, wenn der Benutzer die STRG-Taste drückt. Dieses Flag gilt nur für virtuelle Schlüssel. <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <dt></dt> - <dt>0x10</dt> </dl>                | Die Zugriffstaste wird nur aktiviert, wenn der Benutzer die Alt-Taste drückt. Dieses Flag gilt nur für virtuelle Schlüssel. <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <dt>**0x80**</dt> </dl>                                                                          | Der Eintrag ist zuletzt in einer Zugriffstasten Tabelle. <br/>                                                                                                                                                          |



 

</dd> <dt>

**wansi**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Ein ANSI-Zeichen Wert oder ein Code für den virtuellen Schlüssel, der die Zugriffstaste identifiziert.

</dd> <dt>

**wId**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Ein Bezeichner für die Tastatur Beschleunigung. Dies ist der Wert, der an die Fenster Prozedur übermittelt wird, wenn der Benutzer den angegebenen Schlüssel drückt.

</dd> <dt>

**padding**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Anzahl der eingefügten bytes, um sicherzustellen, dass die Struktur an einer **DWORD** -Grenze ausgerichtet wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **acceltableentry** -Struktur wird für alle Zugriffstasten Tabelleneinträge in der Ressource wiederholt. Der letzte Eintrag in der Tabelle wird mit dem Wert 0x0080 gekennzeichnet.

Sie können die Anzahl der Elemente in der Tabelle berechnen, wenn Sie die Länge der Ressource um acht aufteilen. Anschließend kann die Anwendung nach dem Zufallsprinzip auf die einzelnen Einträge fester Länge zugreifen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**"Kreateacceleratortable"**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)
</dt> <dt>

**Licher**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

