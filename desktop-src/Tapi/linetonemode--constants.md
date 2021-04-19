---
description: Die linetonemode- \_ Konstanten beschreiben verschiedene Auswahlmöglichkeiten, die beim Erzeugen von Zeilen Tönen verwendet werden.
ms.assetid: 7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263
title: LINETONEMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e1b5a8d49c927dfa3d5ec87f9a4830a91d79d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366904"
---
# <a name="linetonemode_-constants"></a>Linetonemode- \_ Konstanten

Die **linetonemode- \_ Konstanten** beschreiben verschiedene Auswahlmöglichkeiten, die beim Erzeugen von Zeilen Tönen verwendet werden.

<dl> <dt>

<span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**linetonemode \_ Beep**
</dt> <dd> <dl> <dt>



Der Ton ist ein Signal, z. b., das zum Ankündigen des Anfangs einer Aufzeichnung verwendet wird. Die genaue Definition ist Dienstanbieter definiert.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**linetonemode- \_ Abrechnung**
</dt> <dd> <dl> <dt>



Der Ton ist ein Abrechnungs Informations Ton, z. b. ein Kreditkarten-Eingabe Aufforderungs-Ton. Die genaue Definition ist Dienstanbieter definiert.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**linetonemode \_ ausgelastet**
</dt> <dd> <dl> <dt>



Der Ton ist ein ausgelasteter Ton. Die genaue Definition ist Dienstanbieter definiert.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**linetonemode \_ Custom**
</dt> <dd> <dl> <dt>



Der Ton ist ein benutzerdefinierter Ton, der durch seine Komponenten Frequenzen des Typs [**linegeneratetone**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone)definiert wird.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**linetonemode- \_ Ringback**
</dt> <dd> <dl> <dt>



Der Ton ist ein ringbackton. Die genaue Definition ist Dienstanbieter definiert.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden. Die nieder wertigen 16 Bits sind reserviert.

Diese Konstanten werden verwendet, um die zu generierenden Töne zu definieren, die bei einem Remote Partei aufrufenden aufgerufen werden. Beachten Sie, dass bei der Ton Erkennung von Nichtbenutzer definierten Tönen diese Konstanten nicht verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




