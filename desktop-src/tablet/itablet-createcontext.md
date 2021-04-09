---
description: Erstellt ein Kontext Objekt, das das angegebene Tablet-Gerät beschreibt.
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: 'ITablet:: kreatecontext-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.CreateContext
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 9f1214f7f9e429b5f9b5b9614c2ccfc7fd1800b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868284"
---
# <a name="itabletcreatecontext-method"></a>ITablet:: kreatecontext-Methode

Erstellt ein Kontext Objekt, das das angegebene Tablet-Gerät beschreibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateContext(
  [in]      HWND                    hWnd,
  [in]      RECT                    *prcInput,
  [in]      DWORD                   dwOptions,
  [in]      TABLET_CONTEXT_SETTINGS *pTCS,
  [in]      CONTEXT_ENABLE_TYPE     cet,
  [out]     ITabletContext          **ppCtx,
  [in, out] TABLET_CONTEXT_ID       *pTcid,
  [in, out] PACKET_DESCRIPTION      **ppPD,
  [in]      ITabletEventSink        *pSink
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Das Fenster, an das der Tablet-Kontext angefügt wird.

</dd> <dt>

*prcinput* \[ in\]
</dt> <dd>

\[in, eindeutig\]

Das frei Hand Eingabe Rechteck.

</dd> <dt>

*dwOptions* \[ in\]
</dt> <dd>

Flags, die Tablet-Kontextoptionen festlegen.

</dd> <dt>

*PTCs* \[ in\]
</dt> <dd>

\[in, eindeutig\]

Ausführliche Informationen über den zu erstellenden Tablet-Kontext.

</dd> <dt>

*MEZ* \[ in\]
</dt> <dd>

Ein Wert, der Kontext Meldungen aktiviert oder deaktiviert, die an das Fenster gesendet werden.

</dd> <dt>

*ppctx* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den neu erstellten Tablet-Kontext.

</dd> <dt>

*ptcid* \[ in, out\]
</dt> <dd>

Der Wert, der das Tablet eindeutig identifiziert.

</dd> <dt>

*pppd* \[ in, out\]
</dt> <dd>

Zeiger auf Informationen zu den Daten, die in den einzelnen Paketen enthalten sind.

</dd> <dt>

*psink* \[ in\]
</dt> <dd>

Das [**itableteventsink**](itableteventsink.md) -Objekt, in das Benachrichtigungs Meldungen gesendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

In der Regel Ruft eine Anwendung die Standardwerte aus der [**iTablet:: getdefaultcontextsettings-Methode**](itablet-getdefaultcontextsettings.md)ab, ändert die Werte entsprechend Ihren Anforderungen und übergibt dann die geänderte Einstellungs Struktur an die **iTablet:: deecontext-Methode**.

> [!Note]  
> Sie müssen die [**itableteventsink-Schnittstelle**](itableteventsink.md) implementieren, wenn Sie die **iTablet:: CreateContext-Methode** aufrufen.

 

Der *dwOptions* -Parameter ist ein Satz von Bitflags, die Kontextoptionen beschreiben. In der folgenden Tabelle werden diese Flags beschrieben.



| FlagName                                | Wert                                                                                                                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TCXO- \_ Rand<br/>                  | 0x00000001<br/>                                                                                                                                                                         | Gibt an, dass der Eingabe Kontext auf dem Tablet einen Rand hat. Der Rand ist ein Bereich außerhalb des angegebenen Eingabe Bereichs, in dem Ereignisse dem Rand des Eingabe Bereichs zugeordnet werden. Diese Funktion erleichtert das Eingeben von Punkten am Rand des Kontexts.<br/> |
| TCXO- \_ prähook<br/>                 | 0x00000002<br/>                                                                                                                                                                         | Der prähook Ruft Pakete vor regulären Kontexten und posthooken ab. Sie erhalten Pakete in der Reihenfolge ihrer Erstellung.<br/>                                                                                                                                                  |
| TCXO- \_ Cursor \_ Zustand<br/>           | 0x00000004<br/>                                                                                                                                                                         | Der TC gibt Pakete zurück, auch wenn der Cursor aktiv ist. Standardmäßig gibt ein TC nur Pakete zurück, wenn der Cursor nicht angezeigt wird.<br/>                                                                                                                                       |
| TCXO \_ kein \_ Cursor \_ nach unten<br/>        | 0x00000008<br/>                                                                                                                                                                         | Der TC gibt keine Pakete zurück, wenn der Cursor nicht angezeigt wird.<br/>                                                                                                                                                                                                       |
| TCXO \_ nicht \_ integriert<br/>         | 0x00000010<br/>                                                                                                                                                                         | Der Kontext ist nicht integriert.<br/>                                                                                                                                                                                                                           |
| TCXO \_ posthook<br/>                | 0x00000020<br/>                                                                                                                                                                         | Posthoochs erhalten Pakete nach regulären Tablet-Kontexten, aber vor dem Systemkontext. Sie erhalten Pakete in umgekehrter Reihenfolge ihrer Erstellung.<br/>                                                                                                                   |
| TCXO \_ - \_ Cursor nicht anzeigen \_<br/>      | 0x00000080<br/>                                                                                                                                                                         | Der TC legt die Cursorposition nicht fest.<br/>                                                                                                                                                                                                                      |
| TCXO \_ - \_ TCS nicht validieren \_<br/>     | 0x00000100<br/>                                                                                                                                                                         | Der TC überprüft nicht die GUIDs, die in den Einstellungen des Tablet-Kontexts an die unterstützten Eigenschaften des Geräts übermittelt werden.<br/>                                                                                                                                      |
| TCXO \_ ermöglicht \_ Flicks<br/>           | 0x00000400<br/>                                                                                                                                                                         | Der TC ermöglicht das Durchführen der Flick Erkennung (Standardmäßig ist dies nur für System Kontexte zulässig), und der Client erhält "SE"- \_ Ereignisse.<br/>                                                                                                               |
| TCXO- \_ Klicks zum Zulassen von \_ Feedback \_<br/>   | 0x00000800<br/>                                                                                                                                                                         | Der TC ermöglicht das Anzeigen von Stift Feedback. Standardmäßig ist dies nur für System Kontexte zulässig.<br/>                                                                                                                                                              |
| TCXO \_ - \_ Feedback zulassen ( \_ Fass)<br/> | 0x00001000<br/>                                                                                                                                                                         | Der TC ermöglicht das Anzeigen von Stift Feedback. Standardmäßig ist dies nur für System Kontexte zulässig.<br/>                                                                                                                                                              |
| Alle TCXO \_<br/>                     | TCXO- \_ Rand \| TCXO \_ prehook \| TCXO- \_ Cursor \_ Status \| TCXO \_ kein \_ Cursor \_ nach unten \| TCXO \_ nicht \_ integriert \| TCXO \_ posthook \| TCXO nicht \_ \_ anzeigen \_ Cursor \| TCXO nicht \_ \_ validieren \_ TCS<br/> | Alle definierten Optionen für den Tablet-Kontext.<br/>                                                                                                                                                                                                                           |
| TCXO- \_ Hook<br/>                    | TCXO- \_ prehook \| TCXO \_ posthook<br/>                                                                                                                                                    | Kombiniert die Funktionen vor Hook und posthook.<br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITablet-Schnittstelle**](itablet.md)
</dt> <dt>

[**Kontext \_ enable \_ Type-Enumeration**](context-enable-type.md)
</dt> <dt>

[**Struktur der Tablet- \_ Kontext \_ Einstellungen**](tablet-context-settings.md)
</dt> <dt>

[**Paket \_ Beschreibungs Struktur**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[**Itabletcontextp-Schnittstelle**](itabletcontextp.md)
</dt> <dt>

[**Itableteventsink-Schnittstelle**](itableteventsink.md)
</dt> </dl>

 

 




