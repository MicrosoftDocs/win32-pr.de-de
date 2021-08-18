---
title: WINBIO_EVENT-Struktur (Winbio \_ types.h)
description: Enthält Statusinformationen, die an die Rückrufroutine gesendet werden, wenn ein Ereignishinweis ausgelöst wird.
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- WINBIO_EVENT Struktur Windows Biometrieframework-API
- PWINBIO_EVENT Strukturzeiger Windows Biometrieframework-API
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
ms.openlocfilehash: 6e3baab16ee7c3f825f317d7aa2c585cb4d8ae7d6d030b6f59a1555b95343015
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910543"
---
# <a name="winbio_event-structure"></a>WINBIO \_ EVENT-Struktur

Die **WINBIO \_ EVENT-Struktur** enthält Statusinformationen, die an die Rückrufroutine gesendet werden, wenn ein Ereignishinweis ausgelöst wird.

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

**Typ**
</dt> <dd>

Ein -Wert, der den Typ des ausgelösten Dienstanbieterereignishinweises angibt. Der einzige derzeit unterstützte Anbieter ist der Fingerabdrucksensor. Dieser Sensor unterstützt die folgenden Flags.

<dl> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO \_ EVENT \_ FP \_ UNCLAIMED** (Der Sensor hat eine Fingerwischbewegung erkannt, die von der Anwendung oder dem Fenster, das derzeit den Fokus besitzt, nicht angefordert wurde. Der Windows Biometric Framework ruft Ihre Rückruffunktion auf, um anzugeben, dass ein Fingerwischen aufgetreten ist, aber nicht versucht, den Fingerabdruck zu identifizieren.)
</dt> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO \_ EVENT \_ FP \_ UNCLAIMED \_ IDENTIFY** (Der Sensor hat eine Fingerwischbewegung erkannt, die von der Anwendung oder dem Fenster, das derzeit den Fokus besitzt, nicht angefordert wurde. Der Windows Biometric Framework versucht, den Fingerabdruck zu identifizieren und übergibt das Ergebnis dieses Prozesses an Ihre Rückruffunktion.)
</dt> </dl> </dd> <dt>

**Parameter**
</dt> <dd> <dl> <dt>

**Herrenlosen**
</dt> <dd>

Die für die Erfassung biometrischer Stichproben zurückgegebene Struktur.

<dl> <dt>

**UnitId**
</dt> <dd>

Die biometrische Einheit, die das Beispiel generiert hat.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Ein **ULONG-Wert,** der zusätzliche Informationen zum Fehler bei der Erfassung eines biometrischen Beispiels enthält. Wenn eine Erfassung erfolgreich war, wird dieser Parameter auf 0 (null) festgelegt. Für die Fingerabdruckerfassung werden die folgenden Werte definiert:

-   WINBIO \_ FP \_ ZU \_ HOCH
-   WINBIO \_ FP \_ ZU \_ NIEDRIG
-   WINBIO \_ FP \_ ZU \_ LINKS
-   WINBIO \_ FP \_ ZU \_ RECHTS
-   \_WINBIO FP \_ TOO \_ FAST
-   WINBIO \_ FP \_ ZU \_ LANGSAM
-   WINBIO \_ FP \_ POOR \_ QUALITY
-   WINBIO \_ FP \_ ZU \_ VERZERRT
-   WINBIO \_ FP \_ ZU \_ KURZ
-   WINBIO \_ FP \_ MERGE \_ FAILURE

</dd> </dl> </dd> <dt>

**UnclaimedIdentify**
</dt> <dd>

Für biometrische Erfassung und Identifizierung zurückgegebene Struktur. Die Identifizierung bestimmt, ob eine Stichprobe einer vorhandenen biometrischen Vorlage zugeordnet werden kann.

<dl> <dt>

**UnitId**
</dt> <dd>

Die biometrische Einheit, die das Beispiel generiert hat.

</dd> <dt>

**Identität**
</dt> <dd>

Eine [**WINBIO \_ IDENTITY-Struktur,**](winbio-identity.md) die die GUID oder SID des Benutzers enthält, der das biometrische Beispiel bereitstellt.

</dd> <dt>

**SubFactor**
</dt> <dd>

Ein [**WINBIO \_ BIOMETRIC \_ SUBTYPE-Wert,**](winbio-biometric-subtype-constants.md) der den Einem biometrischen Beispiel zugeordneten Unterfaktor angibt. Das Windows Biometric Framework (WBF) unterstützt derzeit nur die Fingerabdruckerfassung und verwendet die folgenden Konstanten, um untergeordnete Typinformationen darzustellen.

-   WINBIO \_ ANSI \_ 381 \_ POS \_ UNKNOWN
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ INDEX \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ MIDDLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ RING \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ LN THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ LS-ZEIGEFINGER \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ LS-MITTELFINGER \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ LENRINGFINGER \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS RH VIER \_ \_ \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS – VIER \_ \_ \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ TWO \_ THUMBS

> [!IMPORTANT]
>
> Versuchen Sie nicht, den für den *SubFactor-Wert* angegebenen Wert zu überprüfen. Der Windows Biometrics Service überprüft den angegebenen Wert, bevor er an Ihre Implementierung übergeben wird. Wenn der Wert **WINBIO \_ SUBTYPE \_ NO \_ INFORMATION** oder **WINBIO \_ SUBTYPE \_ ANY** ist, überprüfen Sie ggf. .

 

</dd> <dt>

**RejectDetail**
</dt> <dd>

Ein **ULONG-Wert,** der zusätzliche Informationen zum Fehler beim Erfassen eines biometrischen Beispiels enthält. Wenn die Erfassung erfolgreich war, wird dieser Parameter auf 0 (null) festgelegt. Für die Fingerabdruckerfassung werden die folgenden Werte definiert:

-   WINBIO \_ FP \_ ZU \_ HOCH
-   WINBIO \_ FP \_ ZU \_ NIEDRIG
-   WINBIO \_ FP \_ ZU \_ LINKS
-   WINBIO \_ FP \_ ZU \_ RECHTS
-   \_WINBIO FP \_ TOO \_ FAST
-   WINBIO \_ FP \_ ZU \_ LANGSAM
-   WINBIO \_ FP \_ POOR \_ QUALITY
-   WINBIO \_ FP \_ ZU \_ VERZERRT
-   WINBIO \_ FP \_ ZU \_ KURZ
-   WINBIO \_ FP \_ MERGE \_ FAILURE

</dd> </dl> </dd> <dt>

**Fehler**
</dt> <dd>

Struktur, die den Erfolg oder Fehler des überwachten Vorgangs angibt.

<dl> <dt>

**ErrorCode**
</dt> <dd>

**HRESULT-Wert,** der S \_ OK oder einen Fehlercode enthält, der aus Berechnungen resultiert, die vom Windows Biometric Framework ausgeführt wurden.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Rufen Sie die [**WinBioRegisterEventMonitor-Funktion**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) auf, um eine Rückrufroutine zum Empfangen von Ereignisbenachrichtigungen vom Windows Biometric Framework zu registrieren. Der Rückruf ist eine benutzerdefinierte Funktion, die Sie für Ihre Anwendung definieren müssen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungsstrukturen](client-application-structures.md)
</dt> <dt>

[**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





