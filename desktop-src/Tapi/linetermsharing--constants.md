---
description: Die linetermsharing- \_ Bitflag-Konstanten beschreiben verschiedene Methoden, mit denen ein Terminal von Zeilen Geräten, Adressen oder Aufrufen gemeinsam genutzt werden kann.
ms.assetid: 50a52a50-4d94-4068-9ea4-bea862400036
title: LINETERMSHARING_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2587621b6362195a610339ba5620b32f1d4f761
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366019"
---
# <a name="linetermsharing_-constants"></a>Linetermsharing- \_ Konstanten

Die **linetermsharing \_** -Bitflag-Konstanten beschreiben verschiedene Methoden, mit denen ein Terminal von Zeilen Geräten, Adressen oder Aufrufen gemeinsam genutzt werden kann.

<dl> <dt>

<span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**linetermsharing \_ Privat**
</dt> <dd> <dl> <dt>



Das Terminal Gerät ist für ein einzeilige Gerät privat.


</dt> </dl> </dd> <dt>

<span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**linetermsharing \_ sharedconf**
</dt> <dd> <dl> <dt>



Das Terminal Gerät kann von mehreren Zeilen verwendet werden. Die [**linesetterminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) -Anforderungen der verschiedenen Terminals werden am Terminal zusammengeführt oder am Terminal übertragen.


</dt> </dl> </dd> <dt>

<span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**linetermsharing \_ sharedexcl**
</dt> <dd> <dl> <dt>



Das Terminal Gerät kann von mehreren Zeilen verwendet werden. Das letzte Zeilen Gerät, für das ein [**linesetterminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) oder [**TSPI \_ linesetterminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) mit dem Terminal für einen bestimmten Terminal Modus ausgeführt wird, verfügt über eine exklusive Verbindung mit dem Terminal für diesen Modus.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Diese Konstanten beschreiben die Klassen von Steuerungs-und Informationsdaten strömen, die direkt zwischen einem Linien Gerät und einem Terminal Gerät (z. b. einem Telefon Satz) weitergeleitet werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

