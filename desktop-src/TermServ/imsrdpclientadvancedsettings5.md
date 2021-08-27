---
title: IMsRdpClientAdvancedSettings5-Schnittstelle
description: Verwaltet erweiterte Clienteinstellungen. Wird von der IMsRdpClientAdvancedSettings4-Schnittstelle abgeleitet.
ms.assetid: a927cd4c-7f70-493e-a4f6-056d0352d56e
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ad2b26697cd3985cc0e39a8ed7345bc4bbe941
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622346"
---
# <a name="imsrdpclientadvancedsettings5-interface"></a>IMsRdpClientAdvancedSettings5-Schnittstelle

Verwaltet erweiterte Clienteinstellungen. Wird von der [**IMsRdpClientAdvancedSettings4-Schnittstelle**](imsrdpclientadvancedsettings4.md) abgeleitet.

Verwenden Sie zum Abrufen einer Instanz dieser Schnittstelle die [**IMsTscAx::AdvancedSettings-Eigenschaft,**](imstscax-advancedsettings.md) um einen [**IMsTscAdvancedSettings-Schnittstellenzeiger**](imstscadvancedsettings-interface.md) abzurufen. Rufen Sie dann [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den **IMsTscAdvancedSettings-Zeiger** auf, und übergeben Sie **IID \_ IMsRdpClientAdvancedSettings5** an **QueryInterface**.

## <a name="members"></a>Member

Die **IMsRdpClientAdvancedSettings5-Schnittstelle** erbt von [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md). **IMsRdpClientAdvancedSettings5** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsRdpClientAdvancedSettings5-Schnittstelle** verfügt über diese Eigenschaften.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Eigenschaft</th>
<th >Zugriffstyp</th>
<th >Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a><br/></td>
<td >Lesen/Schreiben<br/></td>
<td >Der Audioumleitungsmodus. Die <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode-Eigenschaft</strong></a> verfügt über die folgenden möglichen Werte.<br/>
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (audio redirection is enabled and the option for redirection is &quot; Bring to this computer &quot; . Dies ist der Standardmodus.)<br/> </dt> <dd></dd> <dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (audio redirection is enabled and the option is &quot; Leave at remote computer &quot; . Die &quot; Option Auf Remotecomputer verlassen wird nur unterstützt, wenn eine &quot; Remoteverbindung mit einem Hostcomputer hergestellt wird, auf dem Windows Vista ausgeführt wird. Wenn die Verbindung mit einem Hostcomputer besteht, auf dem Windows Server 2008 ausgeführt wird, wird die Option Auf Remotecomputer verlassen &quot; in Nicht wiedergeben &quot; &quot; &quot; geändert.)<br/> </dt> <dd></dd> <dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (Die Audioumleitung ist aktiviert, und der Modus ist &quot; Nicht &quot; wiedergeben.)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td ><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a><br/></td>
<td >Lesen/Schreiben<br/></td>
<td >Gibt die Größe der virtuellen Cachedatei für Bitmaps mit 32 Bits pro Pixel (bpp) an. Der Maximalwert beträgt 48 Megabyte (MB).<br/></td>
</tr>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a><br/></td>
<td >Lesen/Schreiben<br/></td>
<td >Gibt an, ob die Stecknadelschaltfläche auf der Verbindungsleiste angezeigt werden soll. Standardmäßig ist der Wert <strong>TRUE.</strong><br/></td>
</tr>
<tr class="even">
<td ><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a><br/></td>
<td >Lesen/Schreiben<br/></td>
<td >Gibt an, ob der öffentliche Modus aktiviert oder deaktiviert werden soll. Standardmäßig ist der öffentliche Modus auf <strong>FALSE</strong>festgelegt.<br/></td>
</tr>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a><br/></td>
<td >Lesen/Schreiben<br/></td>
<td >Gibt an, ob die Umleitung in der Zwischenablage aktiviert oder deaktiviert werden soll. Standardmäßig ist der Zwischenablageumleitungsmodus auf <strong>TRUE</strong> (aktiviert) festgelegt.<br/></td>
</tr>
<tr class="even">
<td ><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a><br/></td>
<td >Lesen/Schreiben<br/></td>
<td >Gibt an, ob umgeleitete Geräte aktiviert oder deaktiviert werden sollen. Standardmäßig ist der Modus für umgeleitete Geräte auf <strong>FALSE</strong>festgelegt.<br/></td>
</tr>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a><br/></td>
<td >Lesen/Schreiben<br/></td>
<td >Gibt an, ob umgeleitete Point of Service-Geräte aktiviert oder deaktiviert werden sollen. Standardmäßig ist der Modus für umgeleitete Point of Service-Geräte auf <strong>FALSE</strong>festgelegt.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:

-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
-   [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                   |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 ist als FBA7F64E-6783-4405-DA45-FA4A763DABD0 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Remotedesktop-Webverbindung-Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

