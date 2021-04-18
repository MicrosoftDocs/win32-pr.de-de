---
description: Die linecallparamflags- \_ Konstanten beschreiben verschiedene Statusflags für einen-Befehl.
ms.assetid: f323ec9f-5bab-4b5d-93ef-8a552ee0d591
title: LINECALLPARAMFLAGS_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e70fe2721e6fce0ac509b50290b1ec3788f3c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357533"
---
# <a name="linecallparamflags_-constants"></a>Linecallparamflags- \_ Konstanten

Die **linecallparamflags \_** -Konstanten beschreiben verschiedene Statusflags für einen-Befehl.

<dl> <dt>

<span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**linecallparamflags- \_ blockid**
</dt> <dd> <dl> <dt>



Die Absender Identität sollte verborgen sein (Block Aufrufer-ID).


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**linecallparamflags \_ destoffhook**
</dt> <dd> <dl> <dt>



Das Telefon der angerufenen Partei sollte automatisch OFFHOOK werden.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**linecallparamflags im \_ Leerlauf**
</dt> <dd> <dl> <dt>



Der-Befehl sollte aus einer Darstellung im Leerlauf Aussehen und nicht an einem in Bearbeitung befindlichen-Vorgang teilnehmen. Wenn bei Verwendung der [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) -Funktion der Wert für linecallparamflags \_ nicht festgelegt ist und ein vorhandener-Befehl in der Zeile vorhanden ist, unterbricht die Funktion ggf. den vorhandenen-Befehl, um den neuen-Befehl zu erstellen. Wenn kein vorhandener-Befehl vorhanden ist, wird der neue-Befehl von der-Funktion wie angegeben aufgerufen.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**linecallparamflags \_ noholdconference**
</dt> <dd> <dl> <dt>



Dieses Bit wird nur in Verbindung mit [**linesetupconference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) und [**lineprepareaddumconference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)verwendet. Die Adresse, die mit dem aktuellen-Befehl übertragen werden soll, wird im **targetAddress** -Member in [**linecallparametriams**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)angegeben. Der-Beratungs Befehl zeichnet den Wählton nicht physisch vom Switch, sondern durch verschiedene aufrufseinstellerzustände (z. b. unter Wahl und Fortsetzung). Wenn der Verbindungs Gespräch den Status "verbunden" erreicht, wird die Konferenz automatisch eingerichtet. der ursprüngliche-Befehl, der im verbundenen Zustand verbleibt, wechselt in den Status "übertragen". der Beratungs Rückruf wechselt in den Status "übertragen". der hconfcallenter wechselt in den Status "verbunden". Wenn beim Rückruf ein Fehler auftritt (in den Zustand "getrennt", gefolgt von "inaktiv"), wechselt der "hconfcallcenter" auch in den Leerlauf Status, und der ursprüngliche-Befehl (der möglicherweise eine vorhandene Konferenz war, im Fall von " **lineprepareadddeconference**") verbleibt im verbundenen Zustand. Die ursprünglichen Parteien (oder Parteien) nehmen nie an, dass der-Befehl nicht mehr vorhanden ist. Diese Funktion wird häufig verwendet, um einen Supervisor zu einem ACD-Agent-Aufruf hinzuzufügen, wenn dies notwendig ist, um Interaktionen mit einem unate-Aufrufer


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**linecallparamflags \_ onesteptransfer**
</dt> <dd> <dl> <dt>



Dieses Bit wird nur in Verbindung mit [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)verwendet. Er kombiniert den Vorgang von **lineSetupTransfer** , gefolgt von [**linedial**](/windows/desktop/api/Tapi/nf-tapi-linedial) bei einem Rückruf in einem einzigen Schritt. Die Adresse, die gewählt werden soll, wird im **targetAddress** -Member in [**linecallpara**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)festgelegt. Der ursprüngliche Aufruf wird in den *onholdpdingtransfer* -Status versetzt, als ob **lineSetupTransfer** normal aufgerufen wurde, und der Anruf wird normal eingerichtet. Die Anwendung muss weiterhin " [**linecompletetransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) " aufruft, um die Übertragung zu beeinflussen. Diese Funktion wird häufig verwendet, wenn eine Übertragung von einem Server über einen Aufruf Steuerungs Link eines Drittanbieters aufgerufen wird, da solche Verknüpfungen häufig den normalen zweistufigen Prozess nicht unterstützen.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**linecallparamflags- \_ origoffhook**
</dt> <dd> <dl> <dt>



Das Telefon des Absenders sollte automatisch OFFHOOK werden.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**linecallparamflags \_ predictivedial**
</dt> <dd> <dl> <dt>



Dieses Bit wird nur verwendet, wenn ein Aufruf für eine Adresse mit Predictive diwähl-Funktion erfolgt (lineaddrcapflags \_ predictivedialer ist im Member **dwaddrcapflags** in [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)). Das Bit muss aktiviert sein, um die erweiterten Aufrufe und/oder Geräte Überwachungsfunktionen des Geräts zu aktivieren. Wenn dieses Bit nicht auf ON festgelegt ist, wird der Anruf ohne erweiterten Anrufstatus oder Medientyp Überwachung platziert, und es wird keine automatische Übertragung basierend auf dem Anrufstatus initiiert.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**linecallparamflags- \_ sicher**
</dt> <dd> <dl> <dt>



Der-Befehl sollte als sicher eingerichtet werden.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**Linecallparametriams**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**linecompletetransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**linedial**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**lineprepareaddumconference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[**linesetupconference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




