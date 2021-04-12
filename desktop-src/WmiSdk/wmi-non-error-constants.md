---
description: WMI-Rückgabecodes, die den Status anzeigen und keinen Fehler angeben.
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: WMI-nicht-Fehler Konstanten (wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0880c9fda00f03c1fa8b174242bfc84ed9d75ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215445"
---
# <a name="wmi-non-error-constants"></a>WMI-nicht-Fehler-Konstanten

WMI-Rückgabecodes, die den Status anzeigen und keinen Fehler angeben.

Wenn ein Vorgang nicht zu einem Fehler führt, gibt WMI einen der folgenden Codes als **HRESULT** zurück, der den Status des Vorgangs angibt.

> [!Note]  
> Einige Methoden in WMI-Klassen können System-und Netzwerkfehler Codes zurückgeben (z. b. 64). Sie können die Definition dieser Arten von Fehlercodes überprüfen, indem Sie den Befehl **net helpmsg** im Eingabe Aufforderungs Fenster verwenden. Der Befehl **net helpmsg 64** gibt beispielsweise die folgende Meldung zurück: der angegebene Netzwerkname ist nicht mehr verfügbar.

 

In C++ können Sie [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) und **C: \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** als Nachrichten Modul angeben.

<dl> <dt>

<span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM \_ S \_ - \_ Fehler**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Der Vorgang wurde durchgeführt.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM \_ S \_ false**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Es sind keine weiteren Objekte verfügbar, die Anzahl der zurückgegebenen Objekte ist kleiner als die angeforderte Anzahl, oder es handelt sich um das Ende einer Enumeration. Dieser Wert wird auch zurückgegeben, wenn diese Methode mit dem Wert 0 für den *uCount* -Parameter aufgerufen wird.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM \_ S ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

262145 (0x40001)
</dt> <dt>



Es wurde versucht, ein Objekt oder eine Klasse zu erstellen, die bereits vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**WBEM \_ S \_ \_ auf \_ Standard zurücksetzen**
</dt> <dd> <dl> <dt>

262146 (0x40002)
</dt> <dt>



Es wurde eine überschriebene Eigenschaft gelöscht. Dieser Wert wird zurückgegeben, um zu signalisieren, dass der ursprüngliche, nicht überschriebene Wert als Ergebnis der Löschung wieder hergestellt wurde.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM \_ S \_ anders**
</dt> <dd> <dl> <dt>

262147 (0x40003)
</dt> <dt>



Die Elemente (Objekte, Klassen usw.), die verglichen werden, sind nicht identisch.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM \_ S- \_ TimedOut**
</dt> <dd> <dl> <dt>

262148 (0x40004)
</dt> <dt>



Timeout bei einem-Timeout. Dies ist keine Fehlerbedingung. Aus diesem Grund wurden möglicherweise auch einige Ergebnisse zurückgegeben.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM \_ S \_ keine \_ \_ Daten mehr**
</dt> <dd> <dl> <dt>

262149 (0x40005)
</dt> <dt>



Aus der-Enumeration sind keine weiteren Daten verfügbar, und der Benutzer muss die-Enumeration beenden.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**WBEM \_ S- \_ Vorgang \_ abgebrochen**
</dt> <dd> <dl> <dt>

262150 (0x40006)
</dt> <dt>



Der Vorgang wurde absichtlich oder versehentlich abgebrochen.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM \_ S \_ Ausstehend**
</dt> <dd> <dl> <dt>

262151 (0x40007)
</dt> <dt>



Eine Anforderung wird noch ausgeführt, und die Ergebnisse sind noch nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**doppelte WBEM- \_ \_ \_ Objekte**
</dt> <dd> <dl> <dt>

262152 (0x40008)
</dt> <dt>



Im Resultset einer Enumeration wurde mehr als eine Kopie desselben Objekts gefunden.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**WBEM \_ S- \_ Zugriff \_ verweigert**
</dt> <dd> <dl> <dt>

262153 (0x40009 betragen)
</dt> <dt>



Dem Benutzer wurde der Zugriff auf einige, jedoch nicht auf alle Ressourcen verweigert.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**\_ \_ Teilergebnisse von WBEM S \_**
</dt> <dd> <dl> <dt>

262160 (0x40010)
</dt> <dt>



Der Benutzer hat nicht alle Objekte empfangen, die aufgrund von nicht zugänglichen Ressourcen (außer Sicherheitsverletzungen) angefordert wurden.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**eingeschränkter WBEM- \_ \_ \_ Dienst**
</dt> <dd> <dl> <dt>

274433 (0x43001)
</dt> <dt>



Der Anbieter ist in der Lage, den Dienst zu beschränken.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM \_ S \_ indirekt \_ aktualisiert**
</dt> <dd> <dl> <dt>

274434 (0x43002)
</dt> <dt>



Für die zukünftige Verwendung reserviert.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Header<br/>                   | <dl> <dt>Wbemcli. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemcli. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Rückgabe Codes](wmi-return-codes.md)
</dt> </dl>

 

