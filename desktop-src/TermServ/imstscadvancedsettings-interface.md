---
title: IMsTscAdvancedSettings-Schnittstelle
description: Enthält Methoden zum Abrufen und Festlegen von Eigenschaften, die Bitmapzwischenspeicherung, Komprimierung und Drucker- und Zwischenablageumleitung ermöglichen.
ms.assetid: 3385e843-be05-4801-8d59-6395d95686b1
ms.tgt_platform: multiple
keywords:
- IMsTscAdvancedSettings-Remotedesktopdienste
- IMsTscAdvancedSettings-Schnittstelle Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f1156f59178275ff9406299fc553afacd3ce99a0488497f836d147ec1d63547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606197"
---
# <a name="imstscadvancedsettings-interface"></a>IMsTscAdvancedSettings-Schnittstelle

Enthält Methoden zum Abrufen und Festlegen von Eigenschaften, die Bitmapzwischenspeicherung, Komprimierung und Drucker- und Zwischenablageumleitung ermöglichen. Sie können auch Namen von Client-DLLs für virtuelle Kanäle angeben.

Sie erhalten eine Instanz dieser Schnittstelle mithilfe der [**IMsTscAx::AdvancedSettings-Eigenschaft.**](imstscax-advancedsettings.md)

## <a name="members"></a>Member

Die **IMsTscAdvancedSettings-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IMsTscAdvancedSettings** verfügt auch über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IMsTscAdvancedSettings-Schnittstelle** verfügt über diese Eigenschaften.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Eigenschaft</th>
<th style="text-align: left;">Zugriffstyp</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob der Hintergrundeingabemodus aktiviert ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob bitmap caching aktiviert ist.<br/>
<blockquote>
[!Note]<br />
Der Rechtschreibfehler im Namen der Eigenschaft befindet sich in der freigegebenen Version des Steuerelements.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-compress.md"><strong>Komprimieren</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob die Komprimierung aktiviert ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob der containerverhandete Vollbildmodus aktiviert ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob die Drucker- und Zwischenablageumleitung aktiviert ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a><br/></td>
<td style="text-align: left;">Lesegeschützt<br/></td>
<td style="text-align: left;">Gibt den Namen der Datei an, die Symboldaten enthält, auf die beim Anzeigen des Clients im Vollbildmodus zugegriffen wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a><br/></td>
<td style="text-align: left;">Lesegeschützt<br/></td>
<td style="text-align: left;">Gibt den Index des Symbols in der aktuellen Symboldatei an.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a><br/></td>
<td style="text-align: left;">Lesegeschützt<br/></td>
<td style="text-align: left;">Gibt den Namen des aktiven Eingabe-Locale Identifiers an (früher als Tastaturlayout bezeichnet), der für die Verbindung verwendet werden soll.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a><br/></td>
<td style="text-align: left;">Lesegeschützt<br/></td>
<td style="text-align: left;">Gibt die Namen der zu ladenden Client-DLLs des virtuellen Kanals an.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle wurde durch die folgenden Schnittstellen erweitert, und jede neue Schnittstelle erbt alle Methoden und Eigenschaften der vorherigen Schnittstellen:

-   [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
-   [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
-   [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings ist als 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

