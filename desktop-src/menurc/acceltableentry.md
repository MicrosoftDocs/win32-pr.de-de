---
title: ACCELTABLEENTRY-Struktur
description: Beschreibt die Daten in einer einzelnen Zugriffstastentabellenressource. Die hier bereitgestellte Strukturdefinition ist nur zur Erklärung vorgesehen. sie ist in einer Standardheaderdatei nicht vorhanden.
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- ACCELTABLEENTRY-Strukturmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- ACCELTABLEENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ef163c8473c049d3bbe6fbfa8b36876765bf07df0b26cd1d68d3f92c5d315f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972129"
---
# <a name="acceltableentry-structure"></a>ACCELTABLEENTRY-Struktur

Beschreibt die Daten in einer einzelnen Zugriffstastentabellenressource. Die hier bereitgestellte Strukturdefinition ist nur zur Erklärung vorgesehen. sie ist in einer Standardheaderdatei nicht vorhanden.

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

Typ: **WORD**

</dd> <dd>

Beschreibt Eigenschaften der Tastenkombination. Dieser Member kann einen oder mehrere der folgenden Werte aus Winuser.h enthalten.



| Wert                                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> <dt>**FVIRTKEY**</dt> <dt>TRUE</dt> </dl>    | Die Zugriffstaste ist ein [virtueller Schlüsselcode.](/windows/desktop/inputdev/virtual-key-codes) Wenn dieses Flag nicht angegeben wird, wird davon ausgegangen, dass die Zugriffstaste einen ASCII-Zeichencode an gibt. <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <dt>**FNOINVERT-0x02**</dt> <dt></dt> </dl> | Ein Menüelement in der Menüleiste wird nicht hervorgehoben, wenn eine Zugriffstaste verwendet wird. Dieses Attribut ist veraltet und wird nur aus Gründen der Abwärtskompatibilität mit Ressourcendateien beibehalten, die für 16-Bit-Windows.<br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <dt>**FSHIFT-0x04**</dt> <dt></dt> </dl>          | Die Zugriffstaste wird nur aktiviert, wenn der Benutzer die UMSCHALTTASTE drückt. Dieses Flag gilt nur für virtuelle Schlüssel. <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <dt>**FCONTROL-0x08**</dt> <dt></dt> </dl>    | Die Zugriffstaste wird nur aktiviert, wenn der Benutzer die STRG-TASTE drückt. Dieses Flag gilt nur für virtuelle Schlüssel. <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <dt>**FALT-0x10**</dt> <dt></dt> </dl>                | Die Zugriffstaste wird nur aktiviert, wenn der Benutzer die ALT-TASTE drückt. Dieses Flag gilt nur für virtuelle Schlüssel. <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <dt>**0x80**</dt> </dl>                                                                          | Der Eintrag ist der letzte in einer Zugriffstastentabelle. <br/>                                                                                                                                                          |



 

</dd> <dt>

**wAnsi**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Ein ANSI-Zeichenwert oder ein Virtueller Schlüsselcode, der die Zugriffstaste identifiziert.

</dd> <dt>

**Wid**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Ein Bezeichner für die Zugriffstaste. Dies ist der Wert, der an die Fensterprozedur übergeben wird, wenn der Benutzer die angegebene Taste drückt.

</dd> <dt>

**padding**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Anzahl der eingefügten Bytes, um sicherzustellen, dass die Struktur an einer **DWORD-Grenze ausgerichtet** ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **ACCELTABLEENTRY-Struktur** wird für alle Zugriffstastentabelleneinträge in der Ressource wiederholt. Der letzte Eintrag in der Tabelle wird mit dem Wert 0x0080.

Sie können die Anzahl der Elemente in der Tabelle berechnen, wenn Sie die Länge der Ressource durch acht teilen. Anschließend kann Ihre Anwendung nach dem Zufallsprinzip auf die einzelnen Einträge mit fester Länge zugreifen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

