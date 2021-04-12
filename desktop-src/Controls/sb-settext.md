---
title: SB_SETTEXT Meldung (kommstrg. h)
description: Legt den Text im angegebenen Teil eines Status Fensters fest.
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- Windows-Steuerelemente für SB_SETTEXT Meldung
topic_type:
- apiref
api_name:
- SB_SETTEXT
- SB_SETTEXTA
- SB_SETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a466187b4ccd00a974b992eacec11938f45001da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105068"
---
# <a name="sb_settext-message"></a>SB- \_ SetText-Nachricht

Legt den Text im angegebenen Teil eines Status Fensters fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**lobyte**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) des nieder wertigen Worts gibt den NULL basierten Index des festzulegenden Teils an. Wenn das **lobyte** auf SB \_ simpleid festgelegt ist, wird angenommen, dass es sich bei dem Statusfenster um eine Statusleiste im einfachen Modus handelt, d. h. eine Statusleiste mit nur einem Teil.

Das [**Hibyte**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) des nieder wertigen Worts gibt den Typ des Zeichnungs Vorgangs an. Dieser Parameter kann einen der folgenden Werte annehmen.

Das hochwertige Wort von *wParam* wird ignoriert.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span><dl> <dt><strong>1,0</strong></dt> </dl></td>
<td>Der Text wird mit einem Rahmen gezeichnet, der unterhalb der Ebene des Fensters angezeigt wird.<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOBORDERS"></span><span id="sbt_noborders"></span><dl> <dt><strong>SBT_NOBORDERS</strong></dt> </dl></td>
<td>Der Text wird ohne Rahmen gezeichnet.<br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_OWNERDRAW"></span><span id="sbt_ownerdraw"></span><dl> <dt><strong>SBT_OWNERDRAW</strong></dt> </dl></td>
<td>Der Text wird vom übergeordneten Fenster gezeichnet. <br/>
<blockquote>
[!Note]<br />
Eine Statusleiste im einfachen Modus unterstützt das Erstellen von Besitzern nicht.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl> <dt><strong>SBT_POPOUT</strong></dt> </dl></td>
<td>Der Text wird mit einem Rahmen gezeichnet, der höher als die Ebene des Fensters angezeigt wird.<br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_RTLREADING"></span><span id="sbt_rtlreading"></span><dl> <dt><strong>SBT_RTLREADING</strong></dt> </dl></td>
<td>Der Text wird in umgekehrter Richtung zum Text im übergeordneten Fenster angezeigt.<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOTABPARSING"></span><span id="sbt_notabparsing"></span><dl> <dt><strong>SBT_NOTABPARSING</strong></dt> </dl></td>
<td>Tabstopp Zeichen werden ignoriert.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den festzulegenden Text angibt. Wenn *wParam* SBT-Besitzer \_ Zeichnen ist, stellt dieser Parameter 32 Bits von Daten dar. Das übergeordnete Fenster muss die Daten interpretieren und den Text beim Empfang der [**WM \_ DrawItem**](wm-drawitem.md) -Nachricht zeichnen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Die Meldung macht den Teil des geänderten Fensters ungültig, sodass der neue Text angezeigt wird, wenn das Fenster das nächste Mal die WM- [**Zeichnungs \_**](/windows/desktop/gdi/wm-paint) Nachricht empfängt.

Normaler Windows-Anzeige Text von links nach rechts (LTR). Windows kann so *gespiegelt* werden, dass Sprachen wie Hebräisch oder Arabisch angezeigt werden, die von rechts nach links (RTL) gelesen wurden. Wenn SBT \_ RtlReading festgelegt ist, wird die *LPARAM* -Zeichenfolge in der entgegengesetzten Richtung aus dem Text im übergeordneten Fenster gelesen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **SB \_ Settextw** (Unicode) und **SB \_ settexta** (ANSI)<br/>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SB \_ gettext**](sb-gettext.md)
</dt> </dl>

 

