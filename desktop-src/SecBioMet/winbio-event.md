---
title: WINBIO_EVENT Struktur (winbio \_ types. h)
description: Enthält Statusinformationen, die an die Rückruf Routine gesendet werden, wenn ein Ereignis Hinweis ausgelöst wird.
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- WINBIO_EVENT Struktur Windows-Biometrieframework-API
- PWINBIO_EVENT Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_EVENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b6a8301ea5dab7d860e5bd7fb32c69277bad63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346527"
---
# <a name="winbio_event-structure"></a>Winbio- \_ Ereignis Struktur

Die **winbio- \_ Ereignis** Struktur enthält Statusinformationen, die an die Rückruf Routine gesendet werden, wenn ein Ereignis Hinweis ausgelöst wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_EVENT {
  WINBIO_EVENT_TYPE Type;
  union {
    struct {
      WINBIO_UNIT_ID       UnitId;
      WINBIO_REJECT_DETAIL RejectDetail;
    } Unclaimed;
    struct {
      WINBIO_UNIT_ID           UnitId;
      WINBIO_IDENTITY          Identity;
      WINBIO_BIOMETRIC_SUBTYPE SubFactor;
      WINBIO_REJECT_DETAIL     RejectDetail;
    } UnclaimedIdentify;
    struct {
      HRESULT ErrorCode;
    } Error;
  } Parameters;
} WINBIO_EVENT, *PWINBIO_EVENT;
```



## <a name="members"></a>Member

<dl> <dt>

**Type**
</dt> <dd>

Ein-Wert, der den Typ des abgelegten Ereignis Hinweises des Dienstanbieters angibt. Der einzige derzeit unterstützte Anbieter ist der Fingerabdrucksensor. Dieser Sensor unterstützt die folgenden Flags.

<dl> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**Winbio \_ Event \_ FP \_** wurde nicht beansprucht (der Sensor hat einen Fingerring erkannt, der nicht von der Anwendung angefordert wurde, oder das Fenster, das den Fokus besitzt. Der Windows-Biometrieframework Ruft die Rückruffunktion auf, um anzugeben, dass ein Finger schwenken aufgetreten ist, aber nicht versucht, den Fingerabdruck zu identifizieren.)
</dt> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**Winbio \_ Das Ereignis FP hat eine nicht \_ \_ beanspruchte \_ Identifizierung** (der Sensor hat einen Fingerring erkannt, der nicht von der Anwendung angefordert wurde, oder das Fenster, das gerade den Fokus besitzt. Der Windows-Biometrieframework versucht, den Fingerabdruck zu identifizieren, und übergibt das Ergebnis dieses Prozesses an Ihre Rückruffunktion.)
</dt> </dl> </dd> <dt>

**Parameter**
</dt> <dd> <dl> <dt>

**Genommene**
</dt> <dd>

Struktur, die für die biometrische Beispiel Erfassung zurückgegeben wurde.

<dl> <dt>

**Unitid**
</dt> <dd>

Die biometrische Einheit, die das Beispiel generiert hat.

</dd> <dt>

**Rejectdetail**
</dt> <dd>

Ein **ulong** -Wert, der zusätzliche Informationen zu Fehlern bei der Erfassung eines biometrischen Beispiels enthält. Wenn eine Erfassung erfolgreich war, wird dieser Parameter auf 0 (null) festgelegt. Die folgenden Werte sind für die Fingerabdruck Erfassung definiert:

-   winbio \_ FP \_ zu \_ hoch
-   winbio \_ FP \_ zu \_ niedrig
-   winbio \_ FP \_ zu \_ Links
-   winbio \_ FP \_ zu \_ Recht
-   winbio \_ FP \_ zu \_ schnell
-   winbio \_ FP \_ zu \_ langsam
-   winbio \_ fp, \_ schlechte \_ Qualität
-   winbio \_ FP \_ zu \_ verzerrt
-   winbio \_ FP \_ zu \_ kurz
-   winbio \_ FP- \_ Merge- \_ Fehler

</dd> </dl> </dd> <dt>

**Unclaimedidentifizieren**
</dt> <dd>

Struktur, die für die biometrische Erfassung und Identifizierung zurückgegeben wird Identifikation bestimmt, ob eine Stichprobe mit einer vorhandenen biometrischen Vorlage verknüpft werden kann.

<dl> <dt>

**Unitid**
</dt> <dd>

Die biometrische Einheit, die das Beispiel generiert hat.

</dd> <dt>

**Identität**
</dt> <dd>

Eine [**winbio- \_ Identitäts**](winbio-identity.md) Struktur, die die GUID oder SID des Benutzers enthält, der das biometrische Beispiel bereitstellt.

</dd> <dt>

**Teilfaktor**
</dt> <dd>

Ein [**untergeordneter winbio- \_ \_ Untertyp**](winbio-biometric-subtype-constants.md) Wert, der den einem biometrischen Beispiel zugeordneten unter Faktor angibt. Der Windows-Biometrieframework (WBF) unterstützt derzeit nur die Fingerabdruck Erfassung und verwendet die folgenden Konstanten, um Untertyp Informationen darzustellen.

-   Winbio \_ ANSI \_ 381 Torys \_ \_ unbekannt
-   Winbio \_ ANSI \_ 381 \_ POS, \_ RH \_ Thumb
-   Winbio \_ ANSI \_ 381 POS-Zeige- \_ \_ \_ \_ Finger
-   Winbio \_ ANSI \_ 381 \_ Torpo- \_ \_ \_ Mittelfinger
-   Winbio \_ ANSI \_ 381 \_ POS, \_ RH- \_ Klingel \_ Finger
-   Winbio \_ ANSI \_ 381 Torys \_ \_ RH \_ Little \_ Finger
-   Winbio \_ ANSI \_ 381 \_ POS \_ LH \_ Thumb
-   Winbio \_ ANSI \_ 381 Torys \_ \_ LH \_ Index \_ Finger
-   Winbio \_ ANSI \_ 381 \_ POS \_ - \_ Mittel \_ Fingerabdruck
-   Winbio \_ ANSI \_ 381 Torys LH- \_ \_ \_ Klingel \_ Finger
-   Winbio \_ ANSI \_ 381 Torys \_ \_ LH \_ wenig \_ Finger
-   Winbio \_ ANSI 381 Torys mit \_ \_ \_ \_ vier \_ Fingern
-   Winbio \_ ANSI 381 Torys mit \_ \_ \_ \_ vier \_ Fingern
-   Winbio \_ ANSI \_ 381 \_ POS \_ zwei \_ Daumen

> [!IMPORTANT]
>
> Versuchen Sie nicht, den Wert zu überprüfen, der für den *subfaktorwert* angegeben wurde. Der Windows-Biometrie-Dienst überprüft den angegebenen Wert vor der Übergabe an Ihre Implementierung. Wenn der Wert " **winbio \_ SubType \_ No \_ Information** " oder " **winbio \_ SubType \_ any**" lautet, überprüfen Sie ggf. ggf.

 

</dd> <dt>

**Rejectdetail**
</dt> <dd>

Ein **ulong** -Wert, der zusätzliche Informationen über den Fehler beim Erfassen eines biometrischen Beispiels enthält. Wenn die Erfassung erfolgreich war, wird dieser Parameter auf 0 (null) festgelegt. Die folgenden Werte sind für die Fingerabdruck Erfassung definiert:

-   winbio \_ FP \_ zu \_ hoch
-   winbio \_ FP \_ zu \_ niedrig
-   winbio \_ FP \_ zu \_ Links
-   winbio \_ FP \_ zu \_ Recht
-   winbio \_ FP \_ zu \_ schnell
-   winbio \_ FP \_ zu \_ langsam
-   winbio \_ fp, \_ schlechte \_ Qualität
-   winbio \_ FP \_ zu \_ verzerrt
-   winbio \_ FP \_ zu \_ kurz
-   winbio \_ FP- \_ Merge- \_ Fehler

</dd> </dl> </dd> <dt>

**Fehler**
</dt> <dd>

-Struktur, die den Erfolg oder Misserfolg des Vorgangs angibt, der überwacht wird.

<dl> <dt>

**ErrorCode**
</dt> <dd>

**HRESULT** -Wert, der S \_ OK enthält, oder ein Fehlercode, der aus Berechnungen resultiert, die vom Windows-Biometrieframework ausgeführt wurden.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Rufen Sie die [**winbioregistereventmonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) -Funktion auf, um eine Rückruf Routine zu registrieren, um Ereignis Benachrichtigungen vom Windows-Biometrieframework zu empfangen. Der Rückruf ist eine benutzerdefinierte Funktion, die Sie für Ihre Anwendung definieren müssen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Strukturen](client-application-structures.md)
</dt> <dt>

[**Winbioregistereventmonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





