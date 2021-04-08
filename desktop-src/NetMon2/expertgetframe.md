---
description: Gibt den angeforderten Frame aus einer geladenen Erfassung zurück.
ms.assetid: efd1cff5-a3a1-4910-b003-25b6e10dad6e
title: Expertgetframe-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2bd02bde8caf157b6df6b1dd772a8f7574df0e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862020"
---
# <a name="expertgetframe-function"></a>Expertgetframe-Funktion

Die Funktion " **expertgetframe** " gibt den angeforderten Frame aus einer geladenen Erfassung zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI ExpertGetFrame(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  DWORD                   Direction,
  _In_  DWORD                   RequestFlags,
  _In_  DWORD                   RequestedFrameNumber,
  _In_  HFILTER                 hFilter,
  _Out_ LPEXPERTFRAMEDESCRIPTOR pEFrameDescriptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hexpertkey* \[ in\]
</dt> <dd>

Ein eindeutiger Experte Bezeichner. Netzwerkmonitor übergibt den *hexpertkey* -Bezeichner an den Experten, wenn er die [**Run**](run.md) -Funktion aufruft.

</dd> <dt>

*Richtung* \[ in\]
</dt> <dd>

Ein Wert, der angibt, wie Netzwerkmonitor nach dem Frame sucht.



| Wert                                                                                                                                                                                         | Bedeutung                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="GET_SPECIFIED_FRAME"></span><span id="get_specified_frame"></span><dl> <dt>**\_angegebenen \_ Frame erhalten**</dt> </dl>              | Gibt den angeforderten Frame zurück.<br/> |
| <span id="GET_FRAME_NEXT_FORWARD"></span><span id="get_frame_next_forward"></span><dl> <dt>**\_Frame \_ weiter \_ leiten**</dt> </dl>    | Gibt den nächsten Frame zurück.<br/>      |
| <span id="GET_FRAME_NEXT_BACKWARD"></span><span id="get_frame_next_backward"></span><dl> <dt>**\_Frame \_ nächste \_ rückwärts**</dt> </dl> | Gibt den vorherigen Frame zurück.<br/>  |



 

</dd> <dt>

*Requestflags* \[ in\]
</dt> <dd>

Die Flags, die angeben, wie Netzwerkmonitor die Anforderung verarbeiten soll. Geben Sie mindestens eines der folgenden Flags an.



| Wert                                                                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAGS_DEFER_TO_UI_FILTER"></span><span id="flags_defer_to_ui_filter"></span><dl> <dt>**Flags \_ werden \_ an \_ UI- \_ Filter zurück verschoben**</dt> </dl> | Bevor Sie den Anzeige Filter Parameter des in *hfilter* angegebenen Experten anwenden, wenden Sie den Anzeige Filter an, den Netzwerkmonitor verwendet, wenn der Experte startet.<br/>                                                                                                                              |
| <span id="FLAGS_ATTACH_PROPERTIES"></span><span id="flags_attach_properties"></span><dl> <dt>**Flags \_ - \_ Eigenschaften anfügen**</dt> </dl>      | Die Eigenschaften, die alle Protokoll Parser mit den beanspruchten Abschnitten dieses Frames suchen, werden an den Frame angefügt. Wenn das-Flag nicht festgelegt ist, wird das **lppropertytable** -Feld der Expertenstruktur von " [**expertenframedescriptor**](expertframedescriptor.md) " (von " **Peer framedescriptor**" zurückgegeben) auf **null** festgelegt.<br/> |



 

</dd> <dt>

*Requestedframenreber* \[ in\]
</dt> <dd>

Die Nummer des angeforderten Frames.

</dd> <dt>

*hfilter* \[ in\]
</dt> <dd>

Ein Handle für den expertenanzeigefilter. Wenn der Experte keinen Anzeige Filter hat, legen Sie den-Parameter auf **null** fest.

</dd> <dt>

*Peer Frame Deskriptor* \[ vorgenommen\]
</dt> <dd>

Die Expertenstruktur von " [**expertenframedescriptor**](expertframedescriptor.md) ", die den Frame bei der Rückgabe beschreibt. Der Experte muss den von dieser Struktur verwendeten Arbeitsspeicher zuordnen und freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, gibt der Rückgabewert den Grund für den Fehler an. Wenn der Rückgabewert nmerr- \_ Experte \_ beendet ist, muss der Experte sofort bereinigen und zurückgeben. der Benutzer hat den expertenlauf abgebrochen.

## <a name="remarks"></a>Bemerkungen

Wenn Sie Flags \_ \_ Eigenschaften anfügen festlegen, benötigt der-Befehl mehr Ressourcen, als wenn Sie das-Flag nicht festlegen. Wenn das Flag nicht festgelegt ist, zeigt ein Zeiger auf den rohrahmen und auf Daten über den Frame. Wenn dieses Flag festgelegt ist, fügt Netzwerkmonitor alle Eigenschaften an den Frame an, indem jeder Parser aufgerufen wird, der einen Teil des Frames beansprucht. Dies kann ein langsamer Prozess sein.

Experten sollten das Flag zum Anfügen von Flags nicht festlegen, \_ \_ es sei denn, die Experten benötigen die Eigenschaften, die Parser an den Frame anfügen. Wenn möglich, sollten Experten die Funktion " **expertgetframe** " ohne das-Flag aufrufen und dann die erforderlichen Daten direkt aus dem Frame extrahieren.

Wenn der Experte " **expertengetframe** " aufruft, ohne das Flag "Flags" \_ Anfügen zu \_ müssen, und die diesem Frame zugeordneten Eigenschaften erfordert (z. b. ein Ereignis), ruft der Experte " **expertgetframe** " mit den gleichen Parametern auf, mit Ausnahme der folgenden:

``` syntax
Direction = EXPERT_GET_SPECIFIED_FRAME;
RequestFlags &= (~EXPERT_DEFER_TO_UI_FILTER) | EXPERT_ATTACH_PROPERTIES;
RequestedFrameNumber= (The actual frame number you want);
hFilter = NULL;
pEFrameDescriptor = (The same one as last time);
```

Mit dem vorangehenden Code wird sichergestellt, dass der Experte den erforderlichen Frame erhält, ohne dass der Filter Code erneut aufgerufen werden muss.

Sie können den *hfilter* -Parameter als **LPVOID** festlegen. Wenn Sie vorhanden ist, übergibt der zurückgegebene Frame diesen Filter. Wenn der Experte keinen Anzeige Filter hat, der an die Funktion übergeben werden soll (wenn *hfilter* **null** ist), wird der zurückgegebene Frame nicht gefiltert.

Die Funktion " **expertgetframe** " kann nur von Experten aufgerufen werden, die die Exportfunktion " [**Run**](run.md) " oder " [**configure**](configure.md) " implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




