---
description: Die setbandwidthinfo-Methode legt die Bandbreiten Informationen fest.
ms.assetid: bf5db456-ea67-4a65-a681-df0741f73fc9
title: 'Itconnection:: setbandwidthinfo-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c17054743f6d47775e994dbfe3b80c7afe1ab68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372313"
---
# <a name="itconnectionsetbandwidthinfo-method"></a>Itconnection:: setbandwidthinfo-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **setbandwidthinfo** -Methode legt die Bandbreiten Informationen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBandwidthInfo(
  [in] BSTR   pModifier,
  [in] DOUBLE Bandwidth
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmodifizierer* \[ in\]
</dt> <dd>

Zeiger auf ein **BSTR** , das den Bereich der festgelegten Bandbreite angibt. Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".

</dd> <dt>

*Bandbreite* \[ in\]
</dt> <dd>

Bandbreite.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                      |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Der *pmodifier* -oder *Bandbreiten* Parameter ist ungültig.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/>   |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Unbekannter Fehler.<br/>                                     |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode ist noch nicht implementiert.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *pmodifier* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.

Referenz: RFC 2327.

Der bandänderungsmodifizierer ist normalerweise entweder CT oder wie folgt:

**Gesamtanzahl der CT-Konferenzen:** Jede Gültigkeits [*Dauer (Time to Live,*](t-tapgloss.md) TTL) auf der MBone oder innerhalb eines bestimmten Multicast Verwaltungsbereichs (in den häufig gestellten Fragen zur MBone-Bandbreite und TTL) ist in den häufig gestellten Fragen zu MBone eine implizite maximale Bandbreite zugeordnet. Wenn die Bandbreite einer Sitzung oder eines Mediums in einer Sitzung von der im Bereich impliziten Bandbreite abweicht, a \` b = CT:... " die Zeile sollte für die Sitzung angegeben werden, wodurch die vorgeschlagene Obergrenze für die verwendete Bandbreite angegeben wird. Der Hauptzweck dieses Konzepts besteht darin, eine ungefähre Vorstellung davon zu erhalten, ob zwei oder mehr Konferenzen gleichzeitig nebeneinander existieren können.

**Als Application-Specific Maximum:** Die Bandbreite wird als anwendungsspezifisch interpretiert, d. h., es wird das Konzept der maximalen Bandbreite der Anwendung sein. Normalerweise stimmt dies mit dem fest, was für die "maximale Bandbreite" der Anwendung festgelegt ist, falls zutreffend.

Beachten Sie, dass CT eine Gesamtbandbreite für alle Medien an allen Standorten liefert. Da eine Bandbreiten Abbildung für ein einzelnes Medium an einem einzigen Standort bietet, kann es sein, dass viele Standorte gleichzeitig senden.

**Erweiterungsmechanismus:** Toolwriter können experimentelle bandänderungsmodifiziererer definieren, indem Sie Ihre modifiziererer mit "X-" versehen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itconnection**](itconnection.md)
</dt> </dl>

 

