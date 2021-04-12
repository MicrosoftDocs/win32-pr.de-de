---
description: Die Win32 \_ serialportconfiguration-WMI-Klasse stellt die Einstellungen für die Datenübertragung an einem Windows-basierten seriellen Anschluss dar. Dies schließt Konfigurationen für das Herstellen einer Verbindung und Fehlerüberprüfung ein.
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Win32_SerialPortConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortConfiguration
- Win32_SerialPortConfiguration.Caption
- Win32_SerialPortConfiguration.Description
- Win32_SerialPortConfiguration.SettingID
- Win32_SerialPortConfiguration.AbortReadWriteOnError
- Win32_SerialPortConfiguration.BaudRate
- Win32_SerialPortConfiguration.BinaryModeEnabled
- Win32_SerialPortConfiguration.BitsPerByte
- Win32_SerialPortConfiguration.ContinueXMitOnXOff
- Win32_SerialPortConfiguration.CTSOutflowControl
- Win32_SerialPortConfiguration.DiscardNULLBytes
- Win32_SerialPortConfiguration.DSROutflowControl
- Win32_SerialPortConfiguration.DSRSensitivity
- Win32_SerialPortConfiguration.DTRFlowControlType
- Win32_SerialPortConfiguration.EOFCharacter
- Win32_SerialPortConfiguration.ErrorReplaceCharacter
- Win32_SerialPortConfiguration.ErrorReplacementEnabled
- Win32_SerialPortConfiguration.EventCharacter
- Win32_SerialPortConfiguration.IsBusy
- Win32_SerialPortConfiguration.Name
- Win32_SerialPortConfiguration.Parity
- Win32_SerialPortConfiguration.ParityCheckEnabled
- Win32_SerialPortConfiguration.RTSFlowControlType
- Win32_SerialPortConfiguration.StopBits
- Win32_SerialPortConfiguration.XOffCharacter
- Win32_SerialPortConfiguration.XOffXMitThreshold
- Win32_SerialPortConfiguration.XOnCharacter
- Win32_SerialPortConfiguration.XOnXMitThreshold
- Win32_SerialPortConfiguration.XOnXOffInFlowControl
- Win32_SerialPortConfiguration.XOnXOffOutFlowControl
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 065d069b261472e3347a115cfbbff652812b6622
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958201"
---
# <a name="win32_serialportconfiguration-class"></a>Win32 \_ serialportconfiguration-Klasse

Die **Win32 \_ serialportconfiguration** - [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt die Einstellungen für die Datenübertragung an einem Windows-basierten seriellen Anschluss dar. Dies schließt Konfigurationen für das Herstellen einer Verbindung und Fehlerüberprüfung ein.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AbortReadWriteOnError;
  uint32  BaudRate;
  boolean BinaryModeEnabled;
  uint32  BitsPerByte;
  boolean ContinueXMitOnXOff;
  boolean CTSOutflowControl;
  boolean DiscardNULLBytes;
  boolean DSROutflowControl;
  boolean DSRSensitivity;
  string  DTRFlowControlType;
  uint32  EOFCharacter;
  uint32  ErrorReplaceCharacter;
  boolean ErrorReplacementEnabled;
  uint32  EventCharacter;
  boolean IsBusy;
  string  Name;
  string  Parity;
  boolean ParityCheckEnabled;
  string  RTSFlowControlType;
  string  StopBits;
  uint32  XOffCharacter;
  uint32  XOffXMitThreshold;
  uint32  XOnCharacter;
  uint32  XOnXMitThreshold;
  uint32  XOnXOffInFlowControl;
  uint32  XOnXOffOutFlowControl;
};
```

## <a name="members"></a>Member

Die **Win32 \_ serialportconfiguration** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ serialportconfiguration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Abortreadschreiteonerror**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fabortonerror")
</dt> </dl>

**True** gibt an, dass Lese-und Schreibvorgänge beendet werden, wenn ein Fehler auftritt. **True** gibt an, dass der Treiber alle Lese-und Schreibvorgänge mit einem Fehlerstatus beendet, wenn ein Fehler auftritt. Der Treiber nimmt keine weiteren Kommunikations Vorgänge an, bis der Fehler von der Anwendung bestätigt wird.

</dd> <dt>

**' Baudrate '**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Baudrate")
</dt> </dl>

Die Baudrate (Bits pro Sekunde), mit der das Kommunikationsgerät betrieben wird.

Beispiel: 9600

</dd> <dt>

**Binarymodeaktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| sbinary")
</dt> </dl>

**True** gibt an, dass Datenübertragungen im binären Modus für den seriellen Anschluss aktiviert werden. Computer Systeme, auf denen Windows ausgeführt wird, erlauben nur binäre Übertragungen über serielle Ports, sodass dieser Wert immer **true** ist.

</dd> <dt>

**Bitsperbyte**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ByteSize")
</dt> </dl>

Anzahl von Bits, die für jedes Byte von Daten für den seriellen Port von Windows übertragen und empfangen werden. Die Zahl kann sich mit Steuerelementen und Fehlerkorrektur Bits (z. b. Paritätsbits) unterscheiden.

Beispiel: 8

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**ContinueXMitOnXOff**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ftxcontinueonxoff")
</dt> </dl>

**True** gibt an, dass Datenübertragungen fortgesetzt werden, wenn der Eingabepuffer in **XOffXMitThreshold** Bytes voll ist und der Treiber den **xoffchararcter** -Wert übertragen hat, um den Empfang von Bytes zu beenden. Der Wert **false** gibt an, dass die Übertragung nicht fortgesetzt wird, bis der Eingabepuffer innerhalb des **XOnXMitThreshold** -Bytes leer ist und der Treiber den **XOnCharacter** -Wert zum Fortsetzen des Empfangs verwendet hat.

</dd> <dt>

**Czoutflowcontrol**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| loutxczflow")
</dt> </dl>

Wenn der Wert **true** ist, wird das Signal "Clear to Send (CTS)" vor der Datenübertragung geprüft. CTS signalisiert, dass beide Geräte der seriellen Verbindung zum Übertragen von Daten bereit sind. Die Datenübertragung wird angehalten, bis das CTS-Signal angegeben wird.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**Verwerdnullbytes**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| f NULL")
</dt> </dl>

**True** gibt an, dass **null** -bytes (Zeichen) beim Empfang verworfen werden.

</dd> <dt>

**DSROutflowControl**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fioutxdsrflow")
</dt> </dl>

**True** gibt an, dass die Datenflusssteuerung aktiviert ist, wenn eine DSR-Bedingung (Data Set Ready) vorliegt. DSR signalisiert, dass die Verbindung von den Geräten der seriellen Verbindung hergestellt wurde. Die DSR-Datenübertragung wird angehalten, bis das DSR-Signal angegeben wird.

</dd> <dt>

**Dsrsensitivität**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| sdsrsensisensitivität")
</dt> </dl>

**True** gibt an, dass der Kommunikationstreiber für den Zustand des DSR-Signals sensibel ist. Der Treiber ignoriert alle empfangenen Bytes, es sei denn, die DSR-Modem-Eingabezeile ist hoch.

</dd> <dt>

**DTRFlowControlType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| sdtrcontrol")
</dt> </dl>

Verwendung der DTR-Fluss Steuerung (Data Terminal Ready), nachdem eine Verbindung hergestellt wurde.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Aktivieren** ("aktivieren")


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Deaktivieren** ("deaktivieren")


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

**Handshake** ("Handshake")


</dt> <dd></dd> </dl>

</dd> <dt>

**EOF-Zeichen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EOF char")
</dt> </dl>

Der Wert des Zeichens, das verwendet wird, um das Ende der Daten zu signalisieren.

Beispiel: ^ Z

</dd> <dt>

**Errorreplacecharacter**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ErrorChar")
</dt> </dl>

Der Wert des Zeichens, mit dem Bytes ersetzt werden, die mit einem Paritätsfehler empfangen wurden.

Beispiel: ^ C

</dd> <dt>

**Errorreplacementaktivierte**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ferrorchar")
</dt> </dl>

**True** gibt an, dass mit Paritäts Fehlern empfangene Bytes durch den Wert **errorreplacecharacter** ersetzt werden. Zeichen mit Paritäts Fehlern werden nur ersetzt, wenn diese Eigenschaft den Wert **true** hat und die Parität aktiviert ist.

</dd> <dt>

**EventCharacter**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| evtchar")
</dt> </dl>

Der Wert des Steuer Zeichens, das zum Signalisieren eines Ereignisses verwendet wird, z. b. das Ende der Datei.

Beispiel: ^ e

</dd> <dt>

**IsBusy**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| File Functions-Dateifunktionen \| ")
</dt> </dl>

**True** gibt an, dass der serielle Port ausgelastet ist.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware- \\ \\ mappcemap \\ \\ SerialComm")
</dt> </dl>

Name des seriellen Windows-Ports.

Beispiel: "COM1"

</dd> <dt>

**Parität**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Parität")
</dt> </dl>

Methode der zu verwendenden Paritäts Überprüfung. Parität wird als Fehler Überprüfungs Methode verwendet, bei der ein zusätzliches Paritäts Bit in jeder Dateneinheit enthalten ist. Der Empfänger kann dann die Gültigkeit der Daten überprüfen, indem er die Bits zählt, die festgelegt sind.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**None** ("None")


</dt> <dd>

Die Paritäts Überprüfung wird nicht verwendet.

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Ungerade** ("ungerade")


</dt> <dd>

Legt das Paritätsbit fest, sodass die Anzahl der festgelegten Bits eine ungerade Zahl ist.

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Sogar** ("auch")


</dt> <dd>

Legt das Paritätsbit fest, sodass die Anzahl der festgelegten Bits eine gerade Zahl ist.

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Mark** ("Mark")


</dt> <dd>

Behält die Festlegung des Paritätsbits auf 1 bei.

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Leerzeichen** ("Leerraum")


</dt> <dd>

Lässt das Paritätsbit auf 0 (null) festgelegt.

</dd> </dl>

</dd> <dt>

**Parametercheckaktivierte**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| f Parity")
</dt> </dl>

**True** gibt an, dass die Paritäts Überprüfung aktiviert ist.

</dd> <dt>

**Rzflowcontroltype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Request to Send (RTS)-Fluss Steuerung. RTS wird verwendet, um zu signalisieren, dass Daten für die Übertragung verfügbar sind.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Aktivieren** ("aktivieren")


</dt> <dd>

RTS ist für die Datenübertragungs Sitzung noch nicht vorhanden.

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deaktivieren** ("deaktivieren")


</dt> <dd>

RTS wird ignoriert, nachdem das erste RTS-Signal empfangen wurde.

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Handshake** ("Handshake")


</dt> <dd>

RTS ist deaktiviert, wenn der Übertragungs Puffer mehr als drei Quartale voll ist, und RTS aktiviert ist, wenn der Puffer kleiner als 1-halbist.

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Umschalten ("** umschalten")


</dt> <dd>

RTS ist eingeschaltet, wenn für die Übertragung Daten gepuffert werden.

</dd> </dl>

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**Stoppbits**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Stopbits")
</dt> </dl>

Anzahl der zu verwendenden Stoppbits. Beenden Sie Bits trennen Sie jede Einheit von Daten in einer asynchronen seriellen Verbindung. Sie werden auch fortlaufend gesendet, wenn keine Daten für die Übertragung verfügbar sind.

<dt>

<span id="1"></span>

**1** ("1")


</dt> <dd></dd> <dt>

<span id="1.5"></span>

**1,5** ("1,5")


</dt> <dd></dd> <dt>

<span id="2"></span>

**2** ("2")


</dt> <dd></dd> </dl>

</dd> <dt>

**XOffCharacter**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffChar")
</dt> </dl>

Der Wert des XOFF-Zeichens sowohl für die Übertragung als auch für den Empfang. XOFF ist ein Software Steuerelement, mit dem die Datenübertragung beendet wird (während "RTS" und "CTS" Hardware Steuerelemente sind). XOn nimmt die Übertragung wieder auf.

</dd> <dt>

**XOffXMitThreshold**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| xofflim")
</dt> </dl>

Maximale Anzahl von Bytes, die im Eingabepuffer zulässig sind, bevor das XOff-Zeichen gesendet wird.

</dd> <dt>

**XOnCharacter**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonChar")
</dt> </dl>

Der Wert des XOn-Zeichens für die Übertragung und den Empfang. XOn ist ein Software Steuerelement, mit dem die Datenübertragung fortgesetzt werden kann (während RTS und CTS Hardware Steuerelemente sind). XOFF beendet die Übertragung.

</dd> <dt>

**XOnXMitThreshold**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonLim")
</dt> </dl>

Mindestanzahl von Bytes, die im Eingabepuffer zulässig sind, bevor das XON-Zeichen gesendet wird. Diese Eigenschaft funktioniert in Verbindung mit **XOffXMitThreshold** , um die Rate zu steuern, mit der Daten übertragen werden.

</dd> <dt>

**XOnXOffInFlowControl**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| finx")
</dt> </dl>

**True** gibt an, dass die "XON/XOFF"-Fluss Steuerung beim Empfang verwendet wird. **True** gibt an, dass der **XOffCharacter** -Wert gesendet wird, wenn der Eingabepuffer in die **XOffXMitThreshold** -Bytes voll ist, und der **XOnCharacter** -Wert gesendet wird, wenn der Eingabepuffer in die **XOnXMitThreshold** -Bytes leer ist.

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

false

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

TRUE

</dd> </dl>

</dd> <dt>

**XOnXOffOutFlowControl**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| f")
</dt> </dl>

Das **XOnXOffOutFlowControl** -Element gibt an, ob bei der Übertragung die XOn-oder XOFF-Fluss Steuerung verwendet wird Wenn **true**, wird die Übertragung beendet, wenn der **XOffCharacter** -Wert empfangen wird, und wird erneut gestartet, wenn der **XOnCharacter** -Wert empfangen wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Win32-Klasse " **\_ serialportconfiguration** " wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Einstellung**](cim-setting.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> </dl>

 

 
