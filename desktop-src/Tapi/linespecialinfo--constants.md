---
description: Die linespecialinfo \_ -Bitflag-Konstanten beschreiben besondere Informationen, die das Netzwerk verwenden kann, um verschiedene Vorgänge zur Berichterstellung und Netzwerküberwachung zu melden.
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: LINESPECIALINFO_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78154757515ebd5bfa36778795c26ef9fdc96db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358032"
---
# <a name="linespecialinfo_-constants"></a>Linespecialinfo- \_ Konstanten

Die **linespecialinfo \_** -Bitflag-Konstanten beschreiben besondere Informationen, die das Netzwerk verwenden kann, um verschiedene Vorgänge zur Berichterstellung und Netzwerküberwachung zu melden. Dabei handelt es sich um spezielle codierte Audiosequenzen, die am Anfang der aufgezeichneten Ankündigungen der Netzwerkberatung übertragen werden

<dl> <dt>

<span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**linespecialinfo \_ custirreg**
</dt> <dd> <dl> <dt>



Dieser besondere Informations Ton liegt vor einer leeren Zahl, einem AIS, einer Centrex-Nummer und einer nicht funktionierenden Station, dem Zugriffs Code, der nicht gewählt wurde oder bei dem ein Fehler auftritt, oder der manuellen Abfang Operator-Nachricht (Kategorie der Kunden Unregelmäßigkeiten). Linespecialinfo \_ custirreg wird auch gemeldet, wenn die Abrechnungsinformationen abgelehnt werden und die IP-Adresse am Switch blockiert wird.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**linespecialinfo- \_ nocircuit**
</dt> <dd> <dl> <dt>



Dieser besondere Informations Ton geht vor einer keinen Verbindung oder einer Notfall Ankündigung (trunk Blockierung hin-Kategorie).


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**linespecialinfo \_ neu anordnen**
</dt> <dd> <dl> <dt>



Dieser besondere Informations Ton geht vor einer Neuanordnungs Ankündigung (Kategorie der Kategorie der Geräte). Linespecialinfo \_ reorder wird auch gemeldet, wenn das Telefon zu lange offline gehalten wird.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**linespecialinfo ist \_ nicht verfügbar.**
</dt> <dd> <dl> <dt>



Einzelheiten zum speziellen Informations Ton sind nicht verfügbar und werden nicht bekannt werden.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**linespecialinfo \_ unbekannt**
</dt> <dd> <dl> <dt>



Einzelheiten zum speziellen Informations Ton sind zurzeit unbekannt, werden aber später möglicherweise bekannt sein.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden. Die nieder wertigen 16 Bits sind reserviert.

Besondere Informations Töne werden für Beratungs Nachrichten definiert und in der Regel nicht für Abrechnungs-oder Aufsichts Zwecke verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




