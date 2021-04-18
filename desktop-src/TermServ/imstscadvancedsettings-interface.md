---
title: Imstscadvancedsettings-Schnittstelle
description: Enthält Methoden zum Abrufen und Festlegen von Eigenschaften, die das Zwischenspeichern von Bitmaps, die Komprimierung und die Umleitung von Druckern und Zwischenablage aktivieren
ms.assetid: 3385e843-be05-4801-8d59-6395d95686b1
ms.tgt_platform: multiple
keywords:
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: ad4d55df30c940ecc5a5515f13c05a285507499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341608"
---
# <a name="imstscadvancedsettings-interface"></a>Imstscadvancedsettings-Schnittstelle

Enthält Methoden zum Abrufen und Festlegen von Eigenschaften, die das Zwischenspeichern von Bitmaps, die Komprimierung und die Umleitung von Druckern und Zwischenablage aktivieren Sie können auch Namen von Client-DLLs für virtuelle Kanäle angeben.

Sie erhalten eine Instanz dieser Schnittstelle, indem Sie die [**imstscax:: advancedsettings**](imstscax-advancedsettings.md) -Eigenschaft verwenden.

## <a name="members"></a>Member

Die **imstscadvancedsettings** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Imstscadvancedsettings** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **imstscadvancedsettings** -Schnittstelle verfügt über diese Eigenschaften.



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
<td style="text-align: left;"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowbackgroundinput</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob der Hintergrund Eingabemodus aktiviert ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>Bitmapperistenz</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob bitmapcaching aktiviert ist.<br/>
<blockquote>
[!Note]<br />
Der Rechtschreibfehler im Namen der Eigenschaft ist in der veröffentlichten Version des Steuer Elements.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-compress.md"><strong>Komprimieren</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob die Komprimierung aktiviert ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>Containerhandledfullscreen</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob der vom Container behandelte Vollbildmodus aktiviert ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>Disablerdpdr</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Gibt an, ob die Umleitung von Drucker und Zwischenablage aktiviert ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a><br/></td>
<td style="text-align: left;">Lesegeschützt<br/></td>
<td style="text-align: left;">Gibt den Namen der Datei mit den Symbol Daten an, auf die zugegriffen wird, wenn der Client im Vollbildmodus angezeigt wird.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a><br/></td>
<td style="text-align: left;">Lesegeschützt<br/></td>
<td style="text-align: left;">Gibt den Index des Symbols in der aktuellen Symbol Datei an.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>Keyboardlayoutstr</strong></a><br/></td>
<td style="text-align: left;">Lesegeschützt<br/></td>
<td style="text-align: left;">Gibt den Namen des aktiven Eingabe Gebiets Schema Bezeichners (früher als Tastaturlayout bezeichnet) für die Verbindung an.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-plugindlls.md"><strong>Plugindlls</strong></a><br/></td>
<td style="text-align: left;">Lesegeschützt<br/></td>
<td style="text-align: left;">Gibt die Namen der zu ladenden Virtual Channel-Client-DLLs an.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle wurde durch die folgenden Schnittstellen erweitert, wobei jede neue Schnittstelle alle Methoden und Eigenschaften der vorherigen Schnittstellen erbt:

-   [**Imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md)
-   [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
-   [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ imstscadvancedsettings ist als 809945cc-4b3b-4a92-a6b0-DBF 9b5s2ef2d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Remotedesktop-Webverbindung Referenz](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

