---
title: Datenschutz Vorlagen (WinInet. h)
description: Die folgenden Datenschutz Ebenen entsprechen den Regeln für das akzeptieren, bedingt akzeptieren oder nicht akzeptieren von Cookies.
ms.assetid: d8dd9c12-b159-4f95-820e-521aeb1526bf
topic_type:
- apiref
api_name:
- PRIVACY_TEMPLATE_NO_COOKIES
- PRIVACY_TEMPLATE_HIGH
- PRIVACY_TEMPLATE_MEDIUM_HIGH
- PRIVACY_TEMPLATE_MEDIUM
- PRIVACY_TEMPLATE_MEDIUM_LOW
- PRIVACY_TEMPLATE_LOW
- PRIVACY_TEMPLATE_CUSTOM
- PRIVACY_TEMPLATE_ADVANCED
- PRIVACY_TEMPLATE_MAX
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9394068721920836f61871ca42471469fd4c592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479269"
---
# <a name="privacy-templates"></a>Datenschutz Vorlagen

Die folgenden Datenschutz Ebenen entsprechen den Regeln für das akzeptieren, bedingt akzeptieren oder nicht akzeptieren von Cookies. Diese Ebenen entsprechen den Einstellungen für den Datenschutz, die auf der Registerkarte Datenschutz in Internet Optionen festgelegt sind. Ausführliche Definitionen finden Sie [unter Datenschutz in Internet Explorer 6](https://www.bing.com/search?q=Privacy+in+Internet+Explorer+6) .

<dl> <dt>

<span id="PRIVACY_TEMPLATE_NO_COOKIES"></span><span id="privacy_template_no_cookies"></span>**Datenschutz \_ Vorlage \_ keine \_ Cookies**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Dies entspricht dem **Blockieren aller Cookies** auf der Schieberegler für die Datenschutzeinstellungen in den **Internet Optionen**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_HIGH"></span><span id="privacy_template_high"></span>**Datenschutz \_ Vorlage \_ hoch**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Dies ist das gleiche wie das **hohe** auf der Schieberegler für die Datenschutzeinstellungen in den **Internet Optionen**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_HIGH"></span><span id="privacy_template_medium_high"></span>**Datenschutz \_ Vorlage \_ Mittel \_ hoch**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Dies ist das gleiche wie bei **Mittel \_ hoch** auf der Schieberegler für die Datenschutzeinstellungen in den **Internet Optionen**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM"></span><span id="privacy_template_medium"></span>**Datenschutz \_ Vorlage \_ Mittel**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Dies ist das gleiche wie bei **Medium** auf der Schieberegler für die Datenschutzeinstellungen in **Internet Optionen**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_LOW_"></span><span id="privacy_template_medium_low_"></span>**Datenschutz \_ Vorlage \_ Mittel \_ niedrig** 
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Dies entspricht dem **niedrigsten auf der Schieberegler für die** Datenschutzeinstellungen in den **Internet Optionen**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_LOW"></span><span id="privacy_template_low"></span>**Datenschutz \_ Vorlage \_ niedrig**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Dies ist das gleiche wie das **akzeptieren aller Cookies** auf der Schieberegler "Datenschutzeinstellungen" unter " **Internet Optionen**".


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_CUSTOM"></span><span id="privacy_template_custom"></span>**Datenschutz \_ Vorlage \_ Benutzer definiert**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



Benutzer definiert. Informationen zum Festlegen von benutzerdefinierten Datenschutzeinstellungen finden Sie unter [Erstellen einer angepassten Datenschutz-Import Datei](https://www.bing.com/search?q=How+to+Create+a+Customized+Privacy+Import+File) .


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_ADVANCED"></span><span id="privacy_template_advanced"></span>**Datenschutz \_ Vorlage \_ erweitert**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Benutzer definiert. Erweiterte Optionen werden im Dialogfeld **Erweiterte Datenschutzeinstellungen** festgelegt, das über die Registerkarte **Datenschutz** in den **Internet Optionen** erreichbar ist.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MAX"></span><span id="privacy_template_max"></span>**Datenschutz \_ Vorlage \_ Max.**
</dt> <dd> <dl> <dt>

Datenschutz \_ Vorlage \_ niedrig
</dt> <dt>



Identisch mit der **Datenschutz \_ Vorlage \_ niedrig**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Privacygetzonepreferencew**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**Privacysetzonepreferencew**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

