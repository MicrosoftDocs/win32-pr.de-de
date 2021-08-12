---
description: Erstellt ein Kontextobjekt, das das angegebene Tablettgerät beschreibt.
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: ITablet::CreateContext-Methode
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
ms.openlocfilehash: 8b67e4c15d40f2da7a616295f10a7762b242fb40d9c0b5f42c00eb51d190cc03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450575"
---
# <a name="itabletcreatecontext-method"></a>ITablet::CreateContext-Methode

Erstellt ein Kontextobjekt, das das angegebene Tablettgerät beschreibt.

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

*hWnd* \[ In\]
</dt> <dd>

Das Fenster, an das der Tablet-Kontext angefügt wird.

</dd> <dt>

*prcInput* \[ In\]
</dt> <dd>

\[in, unique\]

Das Ink-Eingaberechteck.

</dd> <dt>

*dwOptions* \[ In\]
</dt> <dd>

Flags, die Tablet-Kontextoptionen festlegen.

</dd> <dt>

*pTCS* \[ In\]
</dt> <dd>

\[in, unique\]

Ausführliche Informationen zum zu erstellenden Tablet-Kontext.

</dd> <dt>

*( )* \[ In\]
</dt> <dd>

Wert, der das Senden von Kontextmeldungen an das Fenster aktiviert oder deaktiviert.

</dd> <dt>

*ppCtx* \[ out\]
</dt> <dd>

Ein Zeiger auf den neu erstellten Tablet-Kontext.

</dd> <dt>

*pTcid* \[ in, out\]
</dt> <dd>

Wert, der das Tablet eindeutig identifiziert.

</dd> <dt>

*ppPD* \[ in, out\]
</dt> <dd>

Zeiger auf Informationen darüber, welche Daten in den einzelnen Paketen enthalten sind.

</dd> <dt>

*pSink* \[ In\]
</dt> <dd>

Das [**ITabletEventSink-Objekt,**](itableteventsink.md) an das Benachrichtigungsmeldungen gesendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

In der Regel erhält eine Anwendung die Standardwerte aus der [**ITablet::GetDefaultContextSettings-Methode,**](itablet-getdefaultcontextsettings.md)ändert Werte entsprechend ihren Anforderungen und übergibt dann die geänderte Einstellungsstruktur an die **ITablet::CreateContext-Methode.**

> [!Note]  
> Sie müssen die [**ITabletEventSink-Schnittstelle implementieren,**](itableteventsink.md) wenn Sie die **ITablet::CreateContext-Methode aufrufen.**

 

Der *dwOptions-Parameter* ist ein Satz von Bitflags, die Kontextoptionen beschreiben. In der folgenden Tabelle werden diese Flags beschrieben.



| Flagname                                | Wert                                                                                                                                                                                         | Beschreibung                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TCXO \_ MARGIN<br/>                  | 0x00000001<br/>                                                                                                                                                                         | Gibt an, dass der Eingabekontext auf dem Tablet einen Rand hat. Der Rand ist ein Bereich außerhalb des angegebenen Eingabebereichs, in dem Ereignisse dem Rand des Eingabebereichs zugeordnet werden. Dieses Feature erleichtert die Eingabe von Punkten am Rand des Kontexts.<br/> |
| TCXO \_ PREHOOK<br/>                 | 0x00000002<br/>                                                                                                                                                                         | Prehook ruft Pakete vor regulären Kontexten und Posthooks ab. Sie erhalten Pakete in der Reihenfolge ihrer Erstellung.<br/>                                                                                                                                                  |
| \_TCXO-CURSORZUSTAND \_<br/>           | 0x00000004<br/>                                                                                                                                                                         | Der TC gibt Pakete zurück, auch wenn der Cursor hoch ist. Standardmäßig gibt ein TC pakete nur zurück, wenn der Cursor aus ist.<br/>                                                                                                                                       |
| TCXO \_ NO \_ CURSOR \_ DOWN<br/>        | 0x00000008<br/>                                                                                                                                                                         | Der TC gibt keine Pakete zurück, wenn der Cursor heruntergefahren ist.<br/>                                                                                                                                                                                                       |
| TCXO \_ NICHT \_ INTEGRIERT<br/>         | 0x00000010<br/>                                                                                                                                                                         | Der Kontext ist nicht integriert.<br/>                                                                                                                                                                                                                           |
| TCXO \_ POSTHOOK<br/>                | 0x00000020<br/>                                                                                                                                                                         | Posthooks erhalten Pakete nach regulären Tabletkontexten, aber vor dem Systemkontext. Sie erhalten Pakete in umgekehrter Reihenfolge ihrer Erstellung.<br/>                                                                                                                   |
| TCXO \_ DONT \_ SHOW \_ CURSOR<br/>      | 0x00000080<br/>                                                                                                                                                                         | Der TC wird die Cursorposition nicht festlegen.<br/>                                                                                                                                                                                                                      |
| TCXO \_ DONT \_ VALIDATE \_ TCS<br/>     | 0x00000100<br/>                                                                                                                                                                         | Der TC überprüft die in den Tablet-Kontexteinstellungen übergebenen GUIDS nicht anhand der unterstützten Eigenschaften des Geräts.<br/>                                                                                                                                      |
| TCXO \_ ALLOW \_ FLICKS<br/>           | 0x00000400<br/>                                                                                                                                                                         | Der TC lässt die Flickerkennung zu (standardmäßig ist dies nur in Systemkontexten zulässig), und der Client SE \_ FLICK-Ereignisse.<br/>                                                                                                               |
| TCXO \_ ALLOW \_ FEEDBACK \_ TAPS<br/>   | 0x00000800<br/>                                                                                                                                                                         | Der TC lässt das Stiftfeedback zu. Standardmäßig ist dies nur in Systemkontexten zulässig.<br/>                                                                                                                                                              |
| TCXO \_ ALLOW \_ FEEDBACK \_ TC<br/> | 0x00001000<br/>                                                                                                                                                                         | Der TC lässt das Stiftfeedback zu. Standardmäßig ist dies nur in Systemkontexten zulässig.<br/>                                                                                                                                                              |
| TCXO \_ ALL<br/>                     | TCXO \_ MARGIN \| TCXO \_ PREHOOK \| TCXO \_ CURSOR \_ STATE \| TCXO \_ NO \_ CURSOR \_ DOWN \| TCXO \_ NON \_ INTEGRATED \| TCXO \_ POSTHOOK \| TCXO \_ DONT \_ SHOW \_ CURSOR \| TCXO \_ DONT \_ VALIDATE \_ TCS<br/> | Alle definierten Tablet-Kontextoptionen.<br/>                                                                                                                                                                                                                           |
| TCXO \_ HOOK<br/>                    | TCXO \_ PREHOOK \| TCXO \_ POSTHOOK<br/>                                                                                                                                                    | Kombiniert pre-hook- und post-hook-Funktionalität.<br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**ITablet-Schnittstelle**](itablet.md)
</dt> <dt>

[**CONTEXT \_ ENABLE \_ TYPE-Enumeration**](context-enable-type.md)
</dt> <dt>

[**STRUKTUR \_ DER \_ TABLET-KONTEXTEINSTELLUNGEN**](tablet-context-settings.md)
</dt> <dt>

[**\_PAKETBESCHREIBUNGsstruktur**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[**ITabletContextP-Schnittstelle**](itabletcontextp.md)
</dt> <dt>

[**ITabletEventSink-Schnittstelle**](itableteventsink.md)
</dt> </dl>

 

 




