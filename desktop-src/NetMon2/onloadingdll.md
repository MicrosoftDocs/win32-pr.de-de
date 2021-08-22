---
description: Lädt die Monitor-DLL.
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: OnLoadingDLL-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnLoadingDLL
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6049684798d6dda9030abd667c28a62f4b19f9b4e66a831ef4c1d2caa880fb1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676870"
---
# <a name="onloadingdll-function"></a>OnLoadingDLL-Funktion

Die **OnLoadingDLL-Funktion** lädt die Monitor-DLL.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnLoadingDLL(
  _Inout_ HBLOB hFilterBlob,
  _In_    DWORD *pCreateFlags,
  _Out_   char  **ppDefaultName,
  _Out_   char  **ppDescription,
  _Out_   char  **ppDefaultScript,
  _Out_   char  **ppDefaultConfig
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFilterBlob* \[ in, out\]
</dt> <dd>

Ein BLOB, das mcsvc verwendet, um einen Monitor mit verfügbaren NICs abzugleichen. Dieser Parameter enthält immer eine Anforderung für eine [IRTC-Schnittstelle,](irtc.md) sodass die meisten Monitore dem BLOB keine Einträge hinzufügen müssen. Ein benutzerdefinierter Monitor kann jedoch zusätzliche Filterkriterien hinzufügen (z. B. dass der MAC-Typ Ethernet sein muss).

</dd> <dt>

*pCreateFlags* \[ In\]
</dt> <dd>

Die Flags, die angeben, wie MCSVC die Erstellung eines Monitors steuert. Dieser Parameter muss einen der folgenden Werte aufweisen:



| Wert                                                                                                                                                                                                            | Bedeutung                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <dt>**MCS \_ CREATE \_ ONE \_ PER \_ NETCARD**</dt> </dl>          | McSVC stellt sicher, dass für jede NIC nur eine Instanz dieses Monitors vorhanden ist. Eine zweite Instanz kann nur erstellt werden, wenn die erste instanz zerstört wird.<br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <dt>**MCS \_ CREATE \_ CONFIGS \_ BY \_ DEFAULT**</dt> </dl> | Wenn der Monitor über eine interne Standardkonfiguration verfügt, erfordert MCSVC nicht, dass der Benutzer den Monitor konfiguriert, bevor die Instanz erstellt wird.<br/>  |



 

</dd> <dt>

*ppDefaultName* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf die Adresse des Standardnamens des Monitors. McSVC verwendet beim Erstellen von Instanzen des Monitors den Standardnamen.

Wenn der zurückgegebene Standardname beispielsweise "Routermonitor" lautet, lautet die erste Überwachungsinstanz "Routermonitor 1", die zweite "RouterMonitor2" usw. Wenn **NULL** zurückgegeben wird, verwendet MCSVC den Namen der DLL.

</dd> <dt>

*ppDescription* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf die Adresse der Beschreibung des Monitors. Die Beschreibung wird an das Monitorsteuerungstool übergeben, das die Beschreibung verwendet, um dem Benutzer anzugeben, dass der Monitor vorhanden ist. Dieser Parameter kann **NULL** zurückgeben.

</dd> <dt>

*ppDefaultScript* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf die Adresse des HTML-Standardformularskripts, das zum Konfigurieren des Monitors verwendet wird. Obwohl die Instanzen des Monitors ihr eigenes Skript ändern können, laden die meisten Monitore ihr Skript einfach einmal aus einer Datei. Der Wert von *ppDefaultScript* kann **NULL** sein. dann kann der Monitor jedoch nicht extern konfiguriert werden, oder er muss später ein Skript bereitstellen. Es ist effizienter, hier ein Standardskript zur Verfügung zu stellen.

</dd> <dt>

*ppDefaultConfig* \[ out\]
</dt> <dd>

Die Adresse der Standardzeichenfolge, die verwendet wird, um den Monitor beim Erstellen zu konfigurieren. Dieser Parameter kann auf **NULL** festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, lautet der Rückgabewert S OK. Dies \_ entspricht NOERROR.

Wenn die Funktion nicht erfolgreich ist, lässt MCSVC den angegebenen Monitor aus allen Listen aus. danach kann kein Monitor dieses Typs erstellt werden.

## <a name="remarks"></a>Hinweise

Die **OnLoadingDLL-Funktion** wird einmal von MCSVC aufgerufen, wenn sie zum ersten Mal die DLL lädt. Die DLL stellt dann die Standardwerte bereit, die von MCSVC beim Erstellen einer Instanz eines Monitors verwendet werden.

Der Monitor muss den gesamten erforderlichen Arbeitsspeicher für die Zeichenfolgen zuordnen, die an MCSVC zurückgegeben werden. Bei der Rückgabe kopiert MCSVC alle Zeichenfolgen und versucht nicht, die zurückgegebenen Zeichenfolgen frei zu geben.

Der Monitor sollte BLOB-Hilfsfunktionen verwenden, um das Filterblob zu ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




